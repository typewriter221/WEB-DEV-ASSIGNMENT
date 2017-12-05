# WEB-DEV-ASSIGNMENT

<html>
<head><title>Assignment</title></head>
<body> 


<script type="text/JavaScript">
     var x=0;
     function inc(){
              x++;
              document.getElementById("num").innerHTML = x;
          }
    
     var timems = Date.now();
  
     function throttle(fn, wait){
     return function(){
        if(timems + wait - Date.now() < 0){   
          fn;
          timems = Date.now();
          }
        }
     }
</script>


<div style="background-color:#CC99CC; width:13.25%; height:100%; float:left;">
     <button onclick="throttle(inc(), 2000)" id="b1" style="background-color:#CC99FF; padding:10% 35%;">Button 1</button><br/>
     <button id="b2" style="background-color:#CC99FF; padding:10% 35%;">Button 2</button><br/>
     <button id="b3" style="background-color:#CC99FF; padding:10% 35%;">Button 3</button><br/>
     <button id="b4" style="background-color:#CC99FF; padding:10% 35%;">Button 4</button><br/>
</div>

<div style="background-color:#CCFFFF; width:86.75%; height:100%; float:right;">
    <table border="1" width="100%" height="100%" cellpadding="0" cellspacing="0">
        <tr>
           <td style="font-size:32; font-weight:bold; text-align:center;">Number of clicks:<span id="num">0</span></td>
        </tr>
    </table>
</div>

</body>
</html>
