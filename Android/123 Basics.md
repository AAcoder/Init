### How to goto second activity 

Intent intent = new Intent().setClass(this, SecondActivity.class);  
startActivity(intent);

### How to fetch contents from http url

    class JSONAsyncTask extends AsyncTask<Void, Void, String> {

        String input = "";
        JSONAsyncTask(String text){
            input = text;
        }
        @Override
        protected void onPreExecute() {
            super.onPreExecute();

        }

        @Override
        protected String doInBackground(Void... text) {
            try {
                URL url = new URL("http://xyz.net/api/qu");
                HttpURLConnection conn = (HttpURLConnection) url.openConnection();
                conn.setRequestMethod("POST");
                conn.setRequestProperty("Content-Type", "application/json;charset=UTF-8");
                conn.setRequestProperty("Accept", "application/json");
                conn.setDoOutput(true);
                conn.setDoInput(true);

                JSONObject jsonParam = new JSONObject();
                jsonParam.put("language", "en-IN");
                jsonParam.put("inputString", input);
                jsonParam.put("context", "generic");

                DataOutputStream os = new DataOutputStream(conn.getOutputStream());
                os.writeBytes(jsonParam.toString());

                os.flush();
                os.close();
                BufferedReader br = new BufferedReader(new InputStreamReader(conn.getInputStream()));
                StringBuilder sb = new StringBuilder();
                String line;
                while ((line = br.readLine()) != null) {
                    sb.append(line+"\n");
                }
                br.close();
                return sb.toString();
            } catch (Exception e) {
                e.printStackTrace();
            }
            return "Exception";
        }

        protected void onPostExecute(String result) {
            try{
                JSONObject jObject = new JSONObject(result);
                JSONArray jso3 = new JSONArray(jObject.getString("intents"));
                for(int i=0;i<jso3.length();i++)
                {
                    JSONObject command = jso3.getJSONObject(i);
                    if(command.getString("command").equals("search"))
                    {
                        JSONObject parameters = command.getJSONObject("parameters");
                        String url = parameters.getString("url");
                        String userAgent = parameters.getString("useragent");
                        WebView myWebView = (WebView) findViewById(R.id.webview);
                        myWebView.getSettings().setUserAgentString(userAgent);
                        url = url + "&mobile=1";
                        myWebView.loadUrl(url);
                    }
                }
            }catch (Exception e)
            {
                e.printStackTrace();
            }

        }
    }
