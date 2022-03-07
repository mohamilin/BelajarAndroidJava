# Belajar Android Java

## LoginApp
1. Setelah membuat project dengan nama `LoginApp`
2. Logika : Didalam halaman `LoginApp` terdapat `gambar, email, password, dan tombol login`
3. Masuk ke file `activity_main.xml` ketika masuk ke file ini, akan tampil code spt ini :
   ```xml
   <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Hello World!"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintLeft_toLeftOf="parent"
            app:layout_constraintRight_toRightOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

    </androidx.constraintlayout.widget.ConstraintLayout>
   ```
4. Lalu, ketika lakukan penyesuain untuk membuat project ini, Kita ubah `androidx.constraintlayout.widget.ConstraintLayout` menjadi `LinearLayout` dan kita hapus  code yang ada pada tag `TextView`. 
5. sebagaimana pada point nomor 2 : 
   1. kita perlu memberikan tag `ImageView`
        ```xml
        <ImageView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:src="@mipmap/ic_launcher"
            android:layout_marginTop="10dp"
            tools:ignore="MissingConstraints" />
        ```
   2. Selain itu, ketika perlu form untuk `email dan password` : Gunakan tag `com.google.android.material.textfield.TextInputLayout` dan `EditText`
      ```xml
      <com.google.android.material.textfield.TextInputLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="30dp"
            android:hint="@string/email">

            <EditText
                android:layout_width="match_parent"
                android:inputType="textEmailAddress"
                android:layout_height="wrap_content"/>
        </com.google.android.material.textfield.TextInputLayout>
        <com.google.android.material.textfield.TextInputLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="5dp"
            android:hint="@string/password">
            <EditText
                android:layout_width="match_parent"
                android:inputType="textPassword"
                android:layout_height="wrap_content"/>
        </com.google.android.material.textfield.TextInputLayout>
      ``` 
   3. Selanjutnya, kita perlu `button login` : Kita bisa gunakan tag `Button`
      ```xml
        <Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="@string/Login"/>
      ```  
6. Hasil akhirnya :
   ![LoginApp](/assets/loginapp.jpeg)