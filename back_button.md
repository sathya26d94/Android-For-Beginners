# How To implement "Hit back button again to exit the application" functionality

```code
boolean doubleBackToExitPressedOnce = false;

@Override
public void onBackPressed() {
    if (doubleBackToExitPressedOnce) {
        super.onBackPressed();
        return;
    }

    this.doubleBackToExitPressedOnce = true;
    Toast.makeText(this, "Please click BACK again to exit", Toast.LENGTH_SHORT).show();

    new Handler().postDelayed(new Runnable() {

        @Override
        public void run() {
            doubleBackToExitPressedOnce=false;                       
        }
    }, 2000);
} 
```

## Reference
[Back button twice to exit app](https://stackoverflow.com/questions/8430805/clicking-the-back-button-twice-to-exit-an-activity)
