<pre>

//will use current users time zone to give the result
var gdt = new GlideDateTime();
     gs.info("current user timezone"); 
     gs.info(gdt.getValue() );
     gs.info(gdt.getDisplayValue());

gs.info("------------------------");

//corresponding time in EST
var estTimeZone = Packages.java.util.TimeZone.getTimeZone('US/Eastern');
    gdt.setTZ(estTimeZone);    
      gs.info("EST timezone"); 
      gs.info(gdt.getValue());
      gs.info(gdt.getDisplayValue());

gs.info("------------------------");

// corresponding time in IST
var istTimeZone = Packages.java.util.TimeZone.getTimeZone('Asia/Kolkata');
   gdt.setTZ(istTimeZone);
      gs.info("IST timezone"); 
     gs.info(gdt.getValue());
     gs.info(gdt.getDisplayValue());

      
//Note: getValue() will always give time in UTC forma
//DisplayValue() will give time based on users time zone


</pre>

