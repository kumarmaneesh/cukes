# Overview

This is an autogenerated documentation about all available cukes step definitions.

Each steps contains a regular expression pattern and a short description of what this step is intended to be used for.

## General steps

Required dependencies:

**Maven**

```xml
<dependency>
    <groupId>lv.ctco.cukes</groupId>
    <artifactId>cukes-core</artifactId>
    <version>${cukes.version}</version>
</dependency>
```

**Gradle**

```
testCompile("lv.ctco.cukes:cukes-core:${cukes.version}");
```

### given

|Pattern|Description|
|-------|-----------|
|let variable "(.+)" to be random UUID|Generates random UUID and assigns it to a variable|
|let variable "(\S+)" to be random password by matching pattern "([Aa0]+)"|Generates random password by given pattern. Pattern may contain symbils a,A,0. So A is replaced with random capital letter, a - with random letter and 0 - with random number|
|let variable "(\S+)" to be random password with length \d+|Generates random password with given length|
|let variable "(.+)" equal to "(.+)"||
|let variable "(["]\*)" be equal to current timestamp||
|value assertions are case-insensitive||
|resources root is "(.+)"||

## GraphQL steps

Required dependencies:

**Maven**

```xml
<dependency>
    <groupId>lv.ctco.cukes</groupId>
    <artifactId>cukes-graphql</artifactId>
    <version>${cukes.version}</version>
</dependency>
```

**Gradle**

```
testCompile("lv.ctco.cukes:cukes-graphql:${cukes.version}");
```

### given

|Pattern|Description|
|-------|-----------|
|query from file "(.+)"||
|query:||

### then

|Pattern|Description|
|-------|-----------|
|let variable "(.+)" equal to header "(.+)" value||
|response contains an array "(.+)" with object having property "(.+)" with value "(.+)"||
|let variable "(.+)" equal to property "(.+)" value||
|let variable "(.+)" equal to response body||
|response is empty||
|response is not empty||
|response equals to "(.\*)"||
|response body not equal to "(.\*)"||
|response contains "(.+)"||
|response body does not contain "(.+)"||
|response contains property "(.+)" containing phrase "(.\*)"||
|response contains property "(.+)" with value "(.\*)"||
|response contains property "(.+)" with value:||
|response contains property "(.+)" with value other than "(.\*)"||
|response contains property "(.+)" of type "(.+)"||
|response contains an array "(.+)" of size (>=\|>\|<=\|<\|<>) (\d+)||
|response contains an array "(.+)" of size (\d+)||
|response contains an array "(.+)" with value "(.\*)"||
|response does not contain property "(.+)"||
|response contains property "(.+)" matching pattern "(.+)"||
|response contains property "(.+)" not matching pattern "(.+)"||
|status code is (\d+)||
|status code is not (\d+)||
|header "(.+)" is empty||
|header "(.+)" is not empty||
|header "(.+)" equal to "(.+)"||
|header "(.+)" not equal to "(.+)"||
|header "(.+)" contains "(.+)"||
|header "(.+)" does not contain "(.+)"||
|header "(.+)" ends with pattern "(.+)"||

### when

|Pattern|Description|
|-------|-----------|
|the query is executed||

## LDAP steps

Required dependencies:

**Maven**

```xml
<dependency>
    <groupId>lv.ctco.cukes</groupId>
    <artifactId>cukes-ldap</artifactId>
    <version>${cukes.version}</version>
</dependency>
```

**Gradle**

```
testCompile("lv.ctco.cukes:cukes-ldap:${cukes.version}");
```

### given

|Pattern|Description|
|-------|-----------|
|LDAP server URL is "(.+)"||
|LDAP server can be connected by user with DN "(.+)" and password "(.+)"||
|the client imports LDIF:||
|prepare new entity modification||
|change attribute "(.+)" (add\|remove\|replace) value "(.+)"||

### then

|Pattern|Description|
|-------|-----------|
|entity exists||
|entity does not exist||
|entity contains attribute "([a-zA-Z][a-zA-Z0-9\-]\*)"||
|entity does not contain attribute "([a-zA-Z][a-zA-Z0-9\-]\*)"||
|entity contains attribute "([a-zA-Z][a-zA-Z0-9\-]\*)" with value "(.\*)"||
|entity contains attribute "([a-zA-Z][a-zA-Z0-9\-]\*)" with value other than "(.\*)"||
|entity contains attribute "([a-zA-Z][a-zA-Z0-9\-]\*)" with (>=\|>\|<=\|<\|<>) (\d+) values?||
|entity contains attribute "([a-zA-Z][a-zA-Z0-9\-]\*)" with (\d+) values?||
|entity contains attribute "([a-zA-Z][a-zA-Z0-9\-]\*)" matching pattern "(.+)"||
|entity contains attribute "([a-zA-Z][a-zA-Z0-9\-]\*)" not matching pattern "(.+)"||
|entity matches LDIF:||
|search result has size (\d+)||
|search result has size (>=\|>\|<=\|<\|<>) (\d+)||
|take entity with index (\d+) from search results||

### when

|Pattern|Description|
|-------|-----------|
|the client creates entity using LDIF from file "(.+)"||
|the client creates entity using LDIF:||
|the client retrieves entity by DN "(.+)"||
|the client deletes entity with DN "(.+)"||
|the client updates entity with DN "(.+)" using prepared modifications||
|the client searches entities within DN "(.+)" by filter "(.+)"||

## RabbitMQ steps

Required dependencies:

**Maven**

```xml
<dependency>
    <groupId>lv.ctco.cukes</groupId>
    <artifactId>cukes-rabbitmq</artifactId>
    <version>${cukes.version}</version>
</dependency>
```

**Gradle**

```
testCompile("lv.ctco.cukes:cukes-rabbitmq:${cukes.version}");
```

### given

|Pattern|Description|
|-------|-----------|
|bind queue "([a-zA-Z0-9_\-\.:]+)" with routing key "(.+)"||
|bind queue "([a-zA-Z0-9_\-\.:]+)" to exchange "([a-zA-Z0-9_\-\.:]+)" with routing key "(.+)"||
|declare( durable)? exchange "([a-zA-Z0-9_\-\.:]+)" of type "(topic\|direct\|fanout)"||
|declare( durable)? exchange "([a-zA-Z0-9_\-\.:]+)"||
|use exchange "([a-zA-Z0-9_\-\.:]+)" by default||
|reply-to is "(.+)"||
|message body:||
|message body is "(.+)"||
|prepare new message||
|content-type is "(.+)"||
|connecting using username "(.+)" and password "(.+)"||
|virtual host is "(.+)"||
|connecting to host "(.+)"||
|server responds on port (\d+)||
|using SSL||
|not using SSL||

### then

|Pattern|Description|
|-------|-----------|
|message body is empty||
|let variable "(.+)" equal to message body||
|message body contains property "(.+)" with value other than "(.\*)"||
|message body contains property "(.+)" of type "(.+)"||
|message body contains an array "(.+)" of size (>=\|>\|<=\|<\|<>) (\d+)||
|message body contains an array "(.+)" of size (\d+)||
|message body does not contain property "(.+)"||
|message body contains "(.+)"||
|message body does not contain "(.+)"||
|message body contains property "(.+)" containing phrase "(.\*)"||
|message body contains property "(.+)" with value "(.\*)"||
|message body contains an array "(.+)" with value "(.\*)"||
|message body contains property "(.+)" matching pattern "(.+)"||
|message body contains property "(.+)" not matching pattern "(.+)"||
|message body is not empty||
|message body equals to "(.\*)"||
|message body not equal to "(.\*)"||
|wait for message in queue "([a-zA-Z0-9_\-\.:]+)"||
|wait for message in queue "([a-zA-Z0-9_\-\.:]+)" for not more than (\d+) seconds||

### when

|Pattern|Description|
|-------|-----------|
|the client sends message to exchange "([a-zA-Z0-9_\-\.:]+)" with routing key "(.+)"||
|the client sends message with routing key "(.+)"||

## REST steps

Required dependencies:

**Maven**

```xml
<dependency>
    <groupId>lv.ctco.cukes</groupId>
    <artifactId>cukes-rest</artifactId>
    <version>${cukes.version}</version>
</dependency>
```

**Gradle**

```
testCompile("lv.ctco.cukes:cukes-rest:${cukes.version}");
```

### given

|Pattern|Description|
|-------|-----------|
|should wait at most (\d+) ([ ]+) with interval (\d+) ([ ]+) until status code (\d+) or fail with "(["]+)"||
|should wait at most (\d+) ([ ]+) with interval (\d+) ([ ]+) until status code (\d+)||
|should wait at most (\d+) ([ ]+) with interval (\d+) ([ ]+) until property "(["]+)" equal to "(["]+)"||
|should wait at most (\d+) ([ ]+) with interval (\d+) ([ ]+) until property "(["]+)" equal to "(["]+)" or fail with "(["]+)"||
|should wait at most (\d+) ([ ]+) with interval (\d+) ([ ]+) until header "(["]+)" equal to "(["]+)"||
|should wait at most (\d+) ([ ]+) with interval (\d+) ([ ]+) until header "(["]+)" equal to "(["]+)" or fail with "(["]+)"||
|accept "(.+)" mediaTypes||
|param "(.+)" "(.+)"||
|proxy settings are "(http\|https)://([:]+)(?::(\d+))?"||
|username "(.+)" and password "(.+)"||
|authentication type is "(.+)"||
|header (["]+) with value "(.+)"||
|request body is a multipart string "(.+)" with mime-type "(.+)" and control "(.+)"||
|session ID is "(.+)"||
|session ID "(.+)" with value "(.+)"||
|cookie "(.+)" with value "(.+)"||
|baseUri is "(.+)"||
|request body:||
|request body from file "(.+)"||
|request body is a multipart file "(.+)"||
|accept mediaType is JSON||
|content type is JSON||
|request body is a multipart with control "(.+)" from file "(.+)"||
|request body is a multipart with mime-type "(.+)" and control "(.+)" from file "(.+)"||
|request body is a multipart string "(.+)" with control "(.+)"||
|content type is "(.+)"||
|queryParam "(.+)" is "(.+)"||
|formParam "(.+)" is "(.+)"||
|request body "(.+)"||

### then

|Pattern|Description|
|-------|-----------|
|let variable "(.+)" equal to header "(.+)" value||
|let variable "(.+)" equal to property "(.+)" value||
|let variable "(.+)" equal to response body||
|response is empty||
|response is not empty||
|response equals to "(.\*)"||
|response body not equal to "(.\*)"||
|response contains "(.+)"||
|response body does not contain "(.+)"||
|response contains property "(.+)" containing phrase "(.\*)"||
|response contains property "(.+)" with value "(.\*)"||
|response contains property "(.+)" with value:||
|response contains property "(.+)" with value other than "(.\*)"||
|response contains property "(.+)" of type "(.+)"||
|response contains an array "(.+)" of size (>=\|>\|<=\|<\|<>) (\d+)||
|response contains an array "(.+)" of size (\d+)||
|response contains an array "(.+)" with value "(.\*)"||
|response does not contain property "(.+)"||
|response contains property "(.+)" matching pattern "(.+)"||
|response contains property "(.+)" not matching pattern "(.+)"||
|status code is (\d+)||
|status code is not (\d+)||
|header "(.+)" is empty||
|header "(.+)" is not empty||
|header "(.+)" equal to "(.+)"||
|header "(.+)" not equal to "(.+)"||
|header "(.+)" contains "(.+)"||
|header "(.+)" does not contain "(.+)"||
|header "(.+)" ends with pattern "(.+)"||
|a failure is expected||
|response contains properties from json:||
|response contains properties from file "(.+)"||
|it fails with "(.+)"||

### when

|Pattern|Description|
|-------|-----------|
|the client performs (.+) request on "(.+)"||
