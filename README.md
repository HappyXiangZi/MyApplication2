# 实验一

1. **要求**：  验证Activity的生命周期

2. **代码**：

   MainActivity.java文件

   ```java
   package com.example.myapplication;
   
   import android.support.v7.app.AppCompatActivity;
   import android.os.Bundle;
   import android.util.Log;
   
   public class MainActivity extends AppCompatActivity {
       public final static String TAG = "AndroidLiveCycle";
       @Override
       protected void onCreate(Bundle savedInstanceState) {
           super.onCreate(savedInstanceState);
           setContentView(R.layout.constrainlayout);
           Log.d(TAG,"onCreate");
       }
   
       @Override
       protected void onStart() {
           super.onStart();
           Log.d(TAG,"onStart");
       }
   
       @Override
       protected void onResume() {
           super.onResume();
           Log.d(TAG,"onResume");
       }
   
       @Override
       protected void onPause() {
           super.onPause();
           Log.d(TAG,"onPause");
       }
   
       @Override
       protected void onStop() {
           super.onStop();
           Log.d(TAG,"onStop");
       }
   
       @Override
       protected void onRestart() {
           super.onRestart();
           Log.d(TAG,"onRestart");
       }
   
       @Override
       protected void onDestroy() {
           super.onDestroy();
           Log.d(TAG,"onDestroy");
       }
   }
   
   ```

3. **运行结果截图**：

   ![](http://ww1.sinaimg.cn/large/8cc1690dgy1g13dqp2nyjj20fm01qglm.jpg)

   ​								项目启动的时候

   ![](http://ww1.sinaimg.cn/large/8cc1690dgy1g13dseqsa3j20oe01waa4.jpg)

   ​								点击home键的时候

   ![](http://ww1.sinaimg.cn/large/8cc1690dgy1g13dtlm0c6j20fi01ndfu.jpg)

   ​								重新进入项目的时候

   ![](http://ww1.sinaimg.cn/large/8cc1690dgy1g13dusntgdj20o101xglr.jpg)

   ​								点击返回键的时候

# 实验二

1. 题目：Android 布局实验

2. 实验过程

   - 线性布局

     - 代码

     ```
     <?xml version="1.0" encoding="utf-8"?>
     <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
         android:layout_width="match_parent"
         android:layout_height="match_parent"
         android:orientation="vertical" >
         <LinearLayout
             android:layout_width="match_parent"
             android:layout_height="wrap_content">
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="One,One" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="One,two" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="One,three" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="One,four" />
         </LinearLayout>
         <LinearLayout
             android:layout_width="match_parent"
             android:layout_height="wrap_content">
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="two,One" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="two,two" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="two,three" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="two,four" />
         </LinearLayout>
         <LinearLayout
             android:layout_width="match_parent"
             android:layout_height="wrap_content">
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="three,One" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="three,two" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="three,three" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="three,four" />
         </LinearLayout>
         <LinearLayout
             android:layout_width="match_parent"
             android:layout_height="wrap_content">
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="four,One" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="four,two" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="four,three" />
             <Button
                 android:layout_width="wrap_content"
                 android:layout_height="wrap_content"
                 android:text="four,four" />
         </LinearLayout>
     
     </LinearLayout>
     ```

     - 截图：

       ![](http://ww1.sinaimg.cn/large/8cc1690dgy1g13e439o2oj20680aejrh.jpg)

   - 约束布局

     - 代码

       ```
       <?xml version="1.0" encoding="utf-8"?>
       <android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
           xmlns:app="http://schemas.android.com/apk/res-auto"
           xmlns:tools="http://schemas.android.com/tools"
           android:layout_width="match_parent"
           android:layout_height="match_parent">
       
           <Button
               android:id="@+id/buttom1"
               android:layout_width="wrap_content"
               android:layout_height="wrap_content"
               android:layout_marginEnd="8dp"
               android:layout_marginRight="8dp"
               android:background="@android:color/holo_red_dark"
               android:text="red"
               app:layout_constraintEnd_toEndOf="@+id/button5"
               app:layout_constraintHorizontal_bias="0.0"
               app:layout_constraintStart_toStartOf="parent"
               app:layout_constraintTop_toTopOf="parent" />
       
           <Button
               android:id="@+id/button4"
               android:layout_width="75dp"
               android:layout_height="46dp"
               android:layout_marginBottom="8dp"
               android:background="@android:color/holo_orange_dark"
               android:text="orange"
               app:layout_constraintBottom_toTopOf="@+id/guideline3"
               app:layout_constraintEnd_toEndOf="@+id/button7"
               app:layout_constraintStart_toStartOf="@+id/button7"
               app:layout_constraintTop_toTopOf="parent"
               app:layout_constraintVertical_bias="0.0" />
       
           <Button
               android:id="@+id/button5"
               android:layout_width="wrap_content"
               android:layout_height="wrap_content"
               android:layout_marginStart="8dp"
               android:layout_marginLeft="8dp"
               android:background="@color/colorAccent"
               android:text="yellow"
               app:layout_constraintEnd_toEndOf="parent"
               app:layout_constraintHorizontal_bias="1.0"
               app:layout_constraintStart_toStartOf="parent"
               app:layout_constraintTop_toTopOf="parent" />
       
           <android.support.constraint.Guideline
               android:id="@+id/guideline2"
               android:layout_width="wrap_content"
               android:layout_height="wrap_content"
               android:orientation="vertical"
               app:layout_constraintGuide_percent="0.5" />
       
           <Button
               android:id="@+id/button6"
               android:layout_width="wrap_content"
               android:layout_height="48dp"
               android:layout_marginStart="8dp"
               android:layout_marginLeft="8dp"
               android:layout_marginTop="8dp"
               android:layout_marginEnd="16dp"
               android:layout_marginRight="16dp"
               android:layout_marginBottom="8dp"
               android:background="@android:color/holo_green_dark"
               android:text="green"
               app:layout_constraintBottom_toBottomOf="parent"
               app:layout_constraintEnd_toStartOf="@+id/button7"
               app:layout_constraintHorizontal_bias="1.0"
               app:layout_constraintStart_toStartOf="parent"
               app:layout_constraintTop_toTopOf="@+id/guideline3"
               app:layout_constraintVertical_bias="0.0" />
       
           <Button
               android:id="@+id/button7"
               android:layout_width="wrap_content"
               android:layout_height="wrap_content"
               android:layout_marginStart="8dp"
               android:layout_marginLeft="8dp"
               android:layout_marginTop="8dp"
               android:layout_marginEnd="8dp"
               android:layout_marginRight="8dp"
               android:layout_marginBottom="8dp"
               android:background="@android:color/holo_blue_dark"
               android:text="blue"
               app:layout_constraintBottom_toBottomOf="parent"
               app:layout_constraintEnd_toEndOf="parent"
               app:layout_constraintStart_toStartOf="parent"
               app:layout_constraintTop_toTopOf="@+id/guideline3"
               app:layout_constraintVertical_bias="0.0" />
       
           <Button
               android:id="@+id/button8"
               android:layout_width="wrap_content"
               android:layout_height="wrap_content"
               android:layout_marginStart="16dp"
               android:layout_marginLeft="16dp"
               android:layout_marginTop="8dp"
               android:layout_marginEnd="16dp"
               android:layout_marginRight="16dp"
               android:layout_marginBottom="8dp"
               android:background="@color/colorPrimaryDark"
               android:text="indigo"
               app:layout_constraintBottom_toBottomOf="parent"
               app:layout_constraintEnd_toEndOf="parent"
               app:layout_constraintHorizontal_bias="0.0"
               app:layout_constraintStart_toEndOf="@+id/button7"
               app:layout_constraintTop_toTopOf="@+id/guideline3"
               app:layout_constraintVertical_bias="0.0" />
       
           <android.support.constraint.Guideline
               android:id="@+id/guideline3"
               android:layout_width="wrap_content"
               android:layout_height="wrap_content"
               android:orientation="horizontal"
               app:layout_constraintGuide_begin="101dp" />
       
           <Button
               android:id="@+id/button"
               android:layout_width="0dp"
               android:layout_height="wrap_content"
               android:layout_marginStart="8dp"
               android:layout_marginLeft="8dp"
               android:layout_marginTop="8dp"
               android:layout_marginEnd="8dp"
               android:layout_marginRight="8dp"
               android:layout_marginBottom="8dp"
               android:background="@color/colorPrimaryDark"
               android:text="violet"
               app:layout_constraintBottom_toBottomOf="parent"
               app:layout_constraintEnd_toEndOf="parent"
               app:layout_constraintHorizontal_bias="0.498"
               app:layout_constraintStart_toStartOf="parent"
               app:layout_constraintTop_toBottomOf="@+id/button7"
               app:layout_constraintVertical_bias="0.123" />
       
       </android.support.constraint.ConstraintLayout>
       ```

     - 截图：

       ![](http://ww1.sinaimg.cn/large/8cc1690dgy1g13e5mqc35j205k09pt8l.jpg)

   - 表格布局

     - 代码：

       ```
       <?xml version="1.0" encoding="utf-8"?>
       <TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
           xmlns:tools="http://schemas.android.com/tools"
           android:layout_width="match_parent"
           android:layout_height="match_parent" >
           <TableRow>
               <TextView
                   android:text="Open..."
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:layout_weight="1"
                   />
               <TextView
                   android:text="Ctrl-O"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:gravity="right"
       
                   />
           </TableRow>
           <TableRow>
               <TextView
                   android:text="Save..."
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:layout_weight="1"
                   />
               <TextView
                   android:text="Ctrl-S"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:gravity="right"
                   />
           </TableRow>
           <TableRow>
               <TextView
                   android:text="Save as..."
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:layout_weight="1"
                   />
               <TextView
                   android:text="Ctrl+shift+S"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:gravity="right"
                   />
           </TableRow>
           <TableRow
               android:layout_width="match_parent"
               >
       
               <View
                   android:layout_width="match_parent"
                   android:layout_height="2dp"
                   android:background="@android:color/background_dark" />
           </TableRow>
           <TableRow>
               <TextView
                   android:text="X Import..."
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:layout_weight="1"
                   />
           </TableRow>
           <TableRow>
               <TextView
                   android:text="X Export..."
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:layout_weight="1"
                   />
               <TextView
                   android:text="Ctrl+E"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:gravity="right"
                   />
           </TableRow>
           <TableRow
               android:layout_width="match_parent"
               >
       
               <View
                   android:layout_width="match_parent"
                   android:layout_height="2dp"
                   android:background="@android:color/background_dark" />
           </TableRow>
           <TableRow>
               <TextView
                   android:text="Quit"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:layout_weight="1"
                   />
           </TableRow>
       </TableLayout>
       ```

     - 截图：

       ![](http://ww1.sinaimg.cn/large/8cc1690dgy1g13egfcfrmj207509z0so.jpg)

