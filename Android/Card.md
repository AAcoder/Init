<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:card_view="http://schemas.android.com/apk/res-auto"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:clipToPadding="false"
    android:orientation="vertical"
    android:paddingTop="3dp"
    android:paddingRight="5dp"
    android:paddingLeft="5dp">

    <android.support.v7.widget.CardView
        android:id="@+id/card_view"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center"
        card_view:cardBackgroundColor="@android:color/white"
        card_view:cardCornerRadius="@dimen/card_album_radius"
        card_view:cardElevation="1sp"
        card_view:cardUseCompatPadding="true">
        
        Card Contents View
        
    </android.support.v7.widget.CardView>
</LinearLayout>

