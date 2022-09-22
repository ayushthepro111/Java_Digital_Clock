# JavaDigitalClock
A simple Java digital clock developed using Netbeans IDE. The clock is been developed using Java.Util.GregorianCalender Class, which is subclass of Calender which provides the standard calender system. Java Thread is used to refresh the display of digital clock after every second. The Font used for the display of clock, is digital-7 which can be downloaded from [here](http://www.dafont.com/digital-7.font).


## Code
Sample code of DigitalClock() constructor to use GregorianCalender class to display time using simple java threads.
```
public DigitalClock() {
        initComponents();
        new Thread(){
            public void run(){
                
                while(true){
                  
                    Calendar cal=new GregorianCalendar();
                    int hour=cal.get(Calendar.HOUR);
                    int min=cal.get(Calendar.MINUTE);
                    int sec=cal.get(Calendar.SECOND);
                  
                    int AM_PM=cal.get(Calendar.AM_PM);
                    String Am_Pm="";
                    if(AM_PM==1){
                        
                        Am_Pm="PM";
                    }
                    else{
                        Am_Pm="AM";
                    }
                   clocklbl.setText(""+hour+":"+min+":"+sec+" "+Am_Pm); 
                }
            }
        }.start();
    }

```
## Run 
To run the project from the command line, go to the dist folder and
type the following:
```
java -jar "JavaDigitalClock.jar" 
```
