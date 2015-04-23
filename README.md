# NavigationSearchView
Android SearchView with Navigation buttons (Next and previous) to traverse through the results.
This Library helps you to add navigation features in the SearchView widget. NavigationSearchView has two buttons inbuilt, along with the clear search button, that will help you traverse through the search results easily.

#Set Up Guide

Set the class com.example.navigationsearchview.NavigationSearchView to your menuitem for SearchView.
eg:

       ```xml
       
       <item
        android:id="@+id/action_search"
        android:actionLayout="@layout/abc_search_view"
        app:actionViewClass="com.example.navigationsearchview.NavigationSearchView"
        android:icon="@android:drawable/ic_menu_search"
        android:title="@string/action_search"
        app:showAsAction="ifRoom|collapseActionView"/>
        ```
Add following code in your onCreateOptionsMenu

          NavigationSearchView action_search = new NavigationSearchView(mContext);
          mainmenu.findItem(R.id.action_search).setActionView(action_search);
          action_search.setOnQueryTextListener(mQueryListener);
          view v = mainmenu.findItem(R.id.action_search).getActionView();

