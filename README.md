# StaggeredGridView
A RecyclerView that lays out children in a staggered grid formation.

![StaggeredGridView](/zero.gif)  ![StaggeredGridView](/one.gif)  ![StaggeredGridView](/two.gif)  ![StaggeredGridView](/three.gif)

To make a StaggeredGridView, add this StaggeredGridView library to your project and add StaggeredGridView in your layout XML. You can also grab it via Gradle:

Gradle
------------
Step 1. Add it in your root build.gradle at the end of repositories:
```groovy
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```
Step 2. Add the dependency
```groovy
dependencies {
	implementation 'com.github.devta-D:StaggeredGridView:v1.0'
}
```

# Usage
--------
###XML
```xml
    <devta.staggeredview.StaggeredGridView
        android:id="@+id/staggeredGridView"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
```

###java
``` 
  StaggeredGridView staggeredGridView = findViewById(R.id.staggeredGridView);

  List<StaggeredData> staggeredDataList = new ArrayList<>();

  staggeredDataList.add(new StaggeredData(0, "Men", "http://45.58.45.156:1080/e-commerce/male.png"));
  staggeredDataList.add(new StaggeredData(1, "Women", "http://45.58.45.156:1080/e-commerce/female.png"));
  staggeredDataList.add(new StaggeredData(2, "Kids", "http://45.58.45.156:1080/e-commerce/kids.png"));
  staggeredDataList.add(new StaggeredData(3, "Home", "http://45.58.45.156:1080/e-commerce/home.png"));
  staggeredDataList.add(new StaggeredData(4, "Gadgets", "http://45.58.45.156:1080/e-commerce/gadgets.png"));
  staggeredDataList.add(new StaggeredData(5, "Beauty", "http://45.58.45.156:1080/e-commerce/beauty.png"));

  staggeredGridView.setData(staggeredDataList);
  staggeredGridView.setClickListener(this);
```

# NOTE
To catch StaggeredGridView item click listener implement StaggeredItemClickListener into your Activity/Fragment as following:

```
AppCompatActivity implements StaggeredItemClickListener{

    @Override
    public void onStaggeredItemClick(StaggeredData item) {
        //perform your action here
    }
```

## Methods:

You may use the following methods in your code to customize your StaggeredGridView.

*`staggeredGridView.setViewDimensions(min, max);` By using above method you can set staggered view minimum and maximum height and the total of both should be 100.

*`staggeredGridView.setViewMaxWidthInDP(getRandomInt());` By using above method you can set maximum width for staggered view.

Developed By
--------

Divyanshu Tayal
<a href="https://www.linkedin.com/in/divyanshu-tayal-4a95b2aa/">
 <img alt="Follow me on LinkedIn"
 src="http://data.pkmmte.com/temp/social_linkedin_logo.png" />
</a>

<a href="https://tecorb.com/">TecOrb Technologies</a>
