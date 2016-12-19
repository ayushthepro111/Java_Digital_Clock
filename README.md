# JavaDigitalClock
A simple Java digital clock developed using Netbeans IDE


![screenshot from 2016-12-11 22 52 14](https://cloud.githubusercontent.com/assets/11054880/21308099/6d29441e-c5fe-11e6-8839-959c6ed4e0b1.png)

## Code of DigitalCLock() Function : 


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



