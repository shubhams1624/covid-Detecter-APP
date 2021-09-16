# covid-Detecter-APP
package com.shubhamsharma.covid19detecter

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.view.View
import android.widget.Button
import android.widget.TextView

class MainActivity : AppCompatActivity() {
    var count =0
    private lateinit var textView1 : TextView

    private lateinit var textView2 : TextView

    private lateinit var textView3 : TextView

    private lateinit var textView4 : TextView

    private lateinit var textView5 : TextView

    private lateinit var textView6 : TextView

    private  var textView7 : TextView ?= null

    private lateinit var textView8 : TextView


    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)


        textView1 = findViewById(R.id.textView1)

        textView2 = findViewById(R.id.textView2)

        textView3 = findViewById(R.id.textView3)

        textView4 = findViewById(R.id.textView4)

        textView5 = findViewById(R.id.textView5)

        textView6 = findViewById(R.id.textView6)

        textView7 = findViewById(R.id.textView7)

        textView8 = findViewById(R.id.textView8)

        val button1: Button = findViewById(R.id.button1)

        val button2: Button = findViewById(R.id.button2)

        val button3: Button = findViewById(R.id.button3)

        val button4: Button = findViewById(R.id.button4)

        val button5: Button = findViewById(R.id.button5)

        val button6: Button = findViewById(R.id.button6)

        val button7: Button = findViewById(R.id.button7)

        val button8: Button = findViewById(R.id.button8)

        val button9: Button = findViewById(R.id.button9)

        val button10: Button = findViewById(R.id.button10)

        val button11: Button = findViewById(R.id.button11)

        val listener = View.OnClickListener { v ->
            val b = v as Button
        }


        button1.setOnClickListener(listener)
        button2.setOnClickListener(listener)
        button3.setOnClickListener(listener)
        button4.setOnClickListener(listener)
        button5.setOnClickListener(listener)
        button6.setOnClickListener(listener)
        button7.setOnClickListener(listener)
        button8.setOnClickListener(listener)
        button9.setOnClickListener(listener)
        button10.setOnClickListener(listener)
        button10.setOnClickListener(listener)
        button11.setOnClickListener(listener)

        button1.setOnClickListener(object : View.OnClickListener{
            override fun onClick(v: View?) {
                count ++
            }
        })
        button3.setOnClickListener(object : View.OnClickListener{
            override fun onClick(v: View?) {
                count ++
            }
        })
        button5.setOnClickListener(object : View.OnClickListener{
            override fun onClick(v: View?) {
                count ++
            }
        })
        button7.setOnClickListener(object : View.OnClickListener{
            override fun onClick(v: View?) {
                count ++
            }
        })
        button9.setOnClickListener(object : View.OnClickListener{
            override fun onClick(v: View?) {
                count ++
            }
        })
        button11.setOnClickListener(object : View.OnClickListener{
            override fun onClick(v: View?) {
                if (count >= 4 ) {

                    textView7?.append("Please get covid Test done as soon as possible and stay quarantine" +
                            "See the Diet plan in WWW.india.com>health")
                }


                if(count <=3 && count>=1){
                    textView7?.append("Viral fever , show the doctor" +
                            "people with mild Symptoms who are otherwise healthy should manage thier Symtoms at home ")
                }


                if(count==1){
                    textView7?.append("you are healthy , But stay at home and follow Social Distancing")

                }

            }
        })



    }
}
