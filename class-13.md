## Readings: The Past, Present & Future of Local Storage for Web Applications

***

### [The Past, Present & Future of Local Storage for Web Applications](http://diveinto.html5doctor.com/storage.html) - Written by Mark Pilgrim

- > Cookies were invented early in the web's history and they can be used as persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:
  - Cookies are included every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
  - Cookies are included with every HTTP requestm thereby sending data unencrytped over the internet (unless your entire web application is served over SSL)
  - Cookies are limited to about 4 KB of data - enough to slow down your application, but not enough to be terribly useful
- What you do want:
  - a lot of storage space
  - on the client
  - that persists beyond a page refresh
  - and isn't transmitted to the server
- > HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.  
`interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};`
- Tracking changes to the HTML5 Storage Area
  - > If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example, if you set an item to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.  
`if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};`
![Storage Event Object]![Storage](https://user-images.githubusercontent.com/84424910/130327147-fa816a25-a8fd-4084-9354-a2c04c3516b8.JPG)
