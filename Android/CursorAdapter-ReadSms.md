private void fetchInbox() { 
Uri inboxURI = Uri.parse("content://sms/inbox");
String[] reqCols = new String[]{"_id", "address", "body"};
ContentResolver cr = getContentResolver();
Cursor c = cr.query(inboxURI, reqCols, null, null, null);

adapter = new SimpleCursorAdapter(this, R.layout.row, c,
new String[]{"body", "address"}, new int[]{
R.id.lblMsg, R.id.lblNumber}, 0);

lvMsg.setAdapter(adapter);
lvMsg.setOnItemLongClickListener(this);

}


row.xml
<?xml version="1.0" encoding="utf-8"?>
<android.support.v7.widget.CardView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:card_view="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_margin="5dp"
    card_view:cardElevation="5dp">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical">

        <TextView
            android:id="@+id/lblNumber"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="5dp"
            android:textColor="#000"
            android:textStyle="bold" />


        <TextView
            android:id="@+id/lblMsg"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="5dp" />


    </LinearLayout>
</android.support.v7.widget.CardView>
