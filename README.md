# calculator
계산기 프로그램입니다

package com.example.a403.myapplication;

import android.net.Uri;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.support.v7.widget.LinearLayoutCompat;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import com.google.android.gms.appindexing.Action;
import com.google.android.gms.appindexing.AppIndex;
import com.google.android.gms.appindexing.Thing;
import com.google.android.gms.common.api.GoogleApiClient;

public class MainActivity extends AppCompatActivity {
    EditText e1, e2;
    Button b1, b2, b3, b4;
    TextView c1;
    /**
     * ATTENTION: This was auto-generated to implement the App Indexing API.
     * See https://g.co/AppIndexing/AndroidStudio for more information.
     */
    private GoogleApiClient client;


    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        e1 = (EditText) findViewById(R.id.editText);
        e2 = (EditText) findViewById(R.id.editText2);
        b1 = (Button) findViewById(R.id.button);
        b2 = (Button) findViewById(R.id.button2);
        b3 = (Button) findViewById(R.id.button3);
        b4 = (Button) findViewById(R.id.button4);
        c1 = (TextView) findViewById(R.id.textView);
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String num1 = e1.getText().toString();
                String num2 = e2.getText().toString();
                int result = Integer.parseInt(num1) + Integer.parseInt(num2);
                c1.setText("계산결과 :" + result);
            }
        });
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String num1 = e1.getText().toString();
                String num2 = e2.getText().toString();
                int result = Integer.parseInt(num1) - Integer.parseInt(num2);
                c1.setText("계산결과 :" + result);

            }
        });
        b3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String num1 = e1.getText().toString();
                String num2 = e2.getText().toString();
                int result = Integer.parseInt(num1) * Integer.parseInt(num2);
                c1.setText("계산결과 :" + result);

            }
        });
        b4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String num1 = e1.getText().toString();
                String num2 = e2.getText().toString();
                int result = Integer.parseInt(num1) / Integer.parseInt(num2);
                c1.setText("계산결과 :" + result);

            }
        });

    }
}
