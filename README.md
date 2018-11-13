# Bookmark scripts

1. SHORTURL
```javascript
javascript: var a = prompt('Url'); if(a) window.open('https://stlink.xyz/.netlify/functions/generate-route?to=' + a, '_blank');
```

2. FB VIDEO URL
```javascript
javascript: var a = prompt('VIDEO ID'); if (a) window.open('https://graph.facebook.com/v3.1/' + a + '?fields=source&access_token=<access_token>', '_blank');
```

3. IP INFO
```javascript
javascript: var a = prompt('IP HERE'); if (a) window.open('http://ip-api.com/' + a, '_blank');
```

4. RANDOM KEY
```javascript
javascript:var getRandomNumber = (max, min = 0) => { return Math.floor((max - min) * Math.random()) + min; }; var listSymbol = `~!@#$%^&*()-_+=[]}{;:'",<.>/?`.split(''); var lengthSymbol = listSymbol.length; var a = prompt('Plain text'); if (a) var b = prompt('Result', a.split('').reduce((encrypted, c) => { encrypted += c + listSymbol[getRandomNumber(lengthSymbol)]; return encrypted; }, listSymbol[getRandomNumber(lengthSymbol)]));
```

5. ENCODE URL
```javascript
javascript: var a = prompt('URL'); if (a) var b = prompt('ENCODED URL', encodeURIComponent(a));
```

6. DECODE URL
```javascript
javascript: var a = prompt('ENCODED URL'); if (a) var b = prompt('URL', decodeURIComponent(a));
```

7. MD5
```javascript
javascript: var a = prompt('Input'); if (a) { var formData = new FormData(); formData.append('secret', a); fetch('https://cors-anywhere.herokuapp.com/http://md5generator.net', {method: 'post', body: formData}) .then(response => response.text()) .then(html => { var start = html.indexOf('<div id="hash">') + 15; var b = prompt('MD5 of ' + a, html.substr(start, 32)); }); }
```

99. GET FB ID
```javascript
javascript: if(!(-1===location.pathname.indexOf('/events/')))var a=prompt('ID',location.pathname.match(/\d+/g)[0]);else if(document.querySelector('.coverWrap'))var id=document.querySelector('.coverWrap').getAttribute('data-referrerid'),a=prompt('ID',id);else{var check=!1;try{for(var metas=document.getElementsByTagName('meta'),i=0;i<metas.length;i++)if(!!metas[i]&&'al:ios:url'==metas[i].getAttribute('property')){var id=metas[i].getAttribute('content').toString().match(/\d+/g)[0];id.length&&(check=!0),prompt('ID',id)}}catch(b){}if(!check)var a=alert('Cannot GET FBID, Reload and try again')}
```

100. GET FB TOKEN
```javascript
javascript:(function(){var id_app = '165907476854626';var fb_dtsg = document['getElementsByName']('fb_dtsg')[0]['value'];var e = new XMLHttpRequest;var t = '/v1.0/dialog/oauth/confirm';var n = 'fb_dtsg=' + fb_dtsg + '&app_id=' + id_app + '&redirect_uri=fbconnect%3A%2F%2Fsuccess&display=page&access_token=&sdk=&from_post=1&private=&tos=&login=&read=&write=&extended=&social_confirm=&confirm=&seen_scopes=&auth_type=&auth_token=&auth_nonce=&default_audience=&ref=Default&return_format=access_token&domain=&sso_device=ios&__CONFIRM__=1&__user=&__a=1&__dyn=798aD5z5CF-&__req=6&ttstamp=&__rev=';e['open']('POST', t, true);e.setRequestHeader('Content-type', 'application/x-www-form-urlencoded');e['onreadystatechange'] = function () {if (e['readyState'] == 4 && e['status'] == 200) {var token = e['responseText']['match'](/token=(.+)&/)[1];var uid = document['getElementsByName']('target')[0]['value'];}};e.onload = function() {var token = this.responseText.match(/access_token=(\w+)/)[1];prompt('Copy this line:', token);};e['send'](n);})();
```
