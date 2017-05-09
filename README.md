<H1>Simple Android http client</H1>

<H3>In your build.gradle file you must add</H3>

```gradle
maven { url "https://jitpack.io"}
```

<H3>In your app's build.gradle file you must add</H3>

```gradle
compile 'com.github.pethoalpar:HttpUrlConnectionModule:v0.1'
```
<H3>In your java file you can use.</H3>

```java
HttpCall httpCall = new HttpCall();
httpCall.setMethodtype(HttpCall.GET);
httpCall.setUrl(ADDRESS);
new HttpRequest(){
  @Override
    public void onResponse(String response) {
      super.onResponse(response);
      Toast.makeText(getApplicationContext(),response,Toast.LENGTH_SHORT).show();
    }
}.execute(httpCall);
```

```java
HttpCall httpCall = new HttpCall();
httpCall.setMethodtype(HttpCall.POST);
httpCall.setUrl(ADDRESS);
HashMap<String, String> params = new HashMap<>();
params.put("",string);
httpCall.setParams(params);
new HttpRequest(){
  @Override
  public void onResponse(String response) {
    super.onResponse(response);
    Toast.makeText(getApplicationContext(),response,Toast.LENGTH_SHORT).show();
  }
}.execute(httpCall);
```
