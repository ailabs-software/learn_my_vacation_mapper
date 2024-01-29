# Build web server

**Goal:** Serve a dynamic web page from Dart

Go into main.dart.

Import file /vacation_service.dart

Create file with following source:

```
import dart io;

class VacationService
{
  static void start() {
     http bind port 4080;
     
     configure routes;
  }
 
 static void handleHome() {
    res.setContentType(ContentType.html);
   res.writeln("<h1>Hello, world.</h1>");
 }
}
```



edit main.dart as follows:

```
void main (List<String> arguments) {
  VacationService.start();
}
```

