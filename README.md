



##Using polymer in grails 3

####Install Polymer:
```
npm install -g polymer-cli
```

####Initialize project from template:
```
cd src/main/webapp
polymer init app-drawer-template
```
####Update  application.yml:
```
cd /grails-app/conf/application.yml
grails:
    resources:
        pattern: 
            '/**'
    profile: web
    
```
####Copy index.html:
```
create a gsp in grails-app/views ex:poly.gsp
copy content of index.html to poly.gsp
    
```
####Update UrlMappings.groovy:
```
"/admin"(view:"/index")
"/"(view:"/poly")
    
```

####Hot swapping & LiveReload:
```
In build.gadle add in dependencies
compile("org.springframework.boot:spring-boot-devtools")
Add in application.yml
spring:
    devtools:
        restart:
            additional-paths :  src/main/webapp
    
```
