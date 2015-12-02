
#Steps Fod Add Mobs

 1) <code>compile 'com.google.android.gms:play-services-ads:8.3.0'</code>
     Add this in dependencies and sync the project
     
 2) Add permission for INTERNET in manifest
 3) Register AddMobs "https://apps.admob.com/"
 4) After Registering we will get add unit id, use that id in layoyt.xml
 
 3) Layout.xml
     <code>
      <com.google.android.gms.ads.AdView
        android:id="@+id/adView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerHorizontal="true"
        android:layout_alignParentBottom="true"
        ads:adSize="BANNER"
        ads:adUnitId="@string/banner_ad_unit_id">
    </com.google.android.gms.ads.AdView>
     </code>
     
  5) MainActivity.java
     <code>
     AdView mAdView = (AdView) findViewById(R.id.adView);
     AdRequest adRequest = new AdRequest.Builder().build();
     mAdView.loadAd(adRequest);
     </code>
