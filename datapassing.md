# Switch Between Activities
The intent is used for switch between activities. In Android development, the Intent class is a fundamental component of the Android framework used for inter-component communication.

Intent(this@MainActivity, SecondActivity::class.java)

```
val intent = Intent(this@MainActivity, SecondActivity::class.java)
```

`startActivity(intent)` ------> It starts the switching to  activity

[![image](https://i.hizliresim.com/3dawpyb.png)](https://hizliresim.com/3dawpyb)

# Data Passing Between Activities


### Sending Data

```
val intent = Intent(this@MainActivity, SecondActivity::class.java)
intent.putExtra("KEY", "data")
startActivity(intent)
```

```
Intent(this@MainActivity, SecondActivity::class.java)
            .apply{startActivity(this.putExtra(KEY, data))}
```

### Reveiving Data

`val receivedInfo = intent.getStringExtra(KEY)`

get...Extra : It changes depending on the type of data received


