# hello-world
the first project on github-hello world
steps of creating ajax request:
  1. create a XMLHttpRequest
  var xhr = new XMLHttpRequest();
  2. prepare to send the XMLHttpRequest
  xhr.open('get','./data.php?username=admin&password=123',true);
  3. send the XMLHttpRequest
  xhr.send(null);
  4. define callback function
  xhr.onreadystatechange = function(){
    if(xhr.readyState == 4){
      if(xhr.status == 200){
        var response = xhr.responseText;
        if(response == "1"){
          document.getElementById('msg').innerHTML = '登录成功';
        }else if(response == "2"){
          document.getElementById('msg').innerHTML = '用户名或密码有误';
        }
      }
    }
  }
