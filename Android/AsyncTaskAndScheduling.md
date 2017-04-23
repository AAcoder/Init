Async Task

Task that runs in background.

public class FetchProactiveDataAsync extends AsyncTask<Void, Void, Void> {

    private static final String TAG = FetchProactiveDataAsync.class.getName();
    private Context mContext;
    private CommonDataItem.Data_Type dataType;
    public FetchProactiveDataAsync(Context mContext, CommonDataItem.Data_Type dataType) {
        this.mContext = mContext;
        this.dataType = dataType;
    }

    @Override
    protected Void doInBackground(Void... voids) {
        try {
            CommonDataIndex.fetchDataFromFeedAndSave(dataType);
        }
        catch (OutOfMemoryError | Exception e) {
            LogUtils.logHandledException(e);
        }

        return null;
    }

    @Override
    protected void onPostExecute(Void aVoid) {
        super.onPostExecute(aVoid);
    }

    @Override
    protected void onCancelled() {

    }
} 
...................................................................................

Scheduling 

final Handler newsHandler = new Handler();
        newsHandler.postDelayed(new Runnable() {
            public void run() {
                Log.d(TAG, "Fetching news");
                new FetchProactiveDataAsync(getApplicationContext(), CommonDataItem.Data_Type.News).executeOnExecutor(AsyncTask.THREAD_POOL_EXECUTOR);
                newsHandler.postDelayed(this, 600000);
            }
        }, 1000);

