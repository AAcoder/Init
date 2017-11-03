        private boolean downloadAndSaveFlags(Context context, String url, String fileName) {

                if(fileName == null || fileName.isEmpty())
                    return false;

                Bitmap bitmap = downloadBitmap(URL);

                FileOutputStream out = null;
                File file = context.getFilesDir();
                String img_path = file.getAbsolutePath() +
                        File.separator +
                        fileName;

                try {
                    out = new FileOutputStream(img_path);
                    bitmap.compress(Bitmap.CompressFormat.PNG, 100, out);
                } catch (Exception e) {
                    AnalyticsUtils.logHandledException(e);
                    Log.w(TAG, e.getMessage(), e);
                    return false;
                } finally {
                    try {
                        if (out != null) {
                            out.close();
                        }
                    } catch (IOException e) {
                        AnalyticsUtils.logHandledException(e);
                        Log.w(TAG, e.getMessage(), e);
                    }
                }
                Log.i(TAG, "Downloaded and saved image for " + fileName);
                return true;
            }

        public static boolean fileExistsInInternalStorage(Context context, String fileName) {
                File file = context.getFilesDir();
                String filePath = file.getAbsolutePath() +
                        File.separator +
                        fileName;

                File flagFile = new File(filePath);
                return flagFile.exists();
            }
