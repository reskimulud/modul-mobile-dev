# Latihan ViewModel dan LiveData

```groovy
    // view model and live data
    implementation "androidx.activity:activity-ktx:1.4.0"
    implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:2.4.1"
    implementation "androidx.lifecycle:lifecycle-livedata-ktx:2.4.1"
```

## Activity Detail Album

```xml
<?xml version="1.0" encoding="utf-8"?>
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".ui.DetailAlbum">

    <androidx.constraintlayout.widget.ConstraintLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <ImageView
            android:id="@+id/iv_detail_album_picture"
            android:layout_width="150dp"
            android:layout_height="150dp"
            android:layout_marginTop="100dp"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            tools:srcCompat="@tools:sample/avatars" />

        <TextView
            android:id="@+id/tv_detail_title"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="@string/title"
            android:layout_marginTop="24dp"
            android:textSize="18sp"
            android:textStyle="bold"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/iv_detail_album_picture" />

        <TextView
            android:id="@+id/tv_detail_artist"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="@string/artist"
            android:layout_marginTop="8dp"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/tv_detail_title" />

        <TextView
            android:id="@+id/tv_description"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/description"
            android:layout_marginHorizontal="16dp"
            android:layout_marginTop="24dp"
            android:textAlignment="center"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/tv_detail_artist" />

    </androidx.constraintlayout.widget.ConstraintLayout>

</ScrollView>
```
