# Custom Toast Android

- Java
```java
public void customToast(Context context, String message) {
    LayoutInflater layoutInflater = (LayoutInflater) context.getSystemService(Context.LAYOUT_INFLATER_SERVICE);
    View view = layoutInflater.inflate(R.layout.custom_toast, null);
    TextView text = (TextView) view.findViewById(R.id.text);

    text.setText(message);
    
    Toast toast = new Toast(context);
    toast.setDuration(Toast.LENGTH_LONG);
    toast.setView(view);
    toast.show();
}
```

---


- Kotlin
```kotlin
fun customToast(context: Context?, message: String?) {
    val layoutInflater =
        context?.getSystemService(Context.LAYOUT_INFLATER_SERVICE) as LayoutInflater
    val view = layoutInflater.inflate(R.layout.custom_toast, null)
    val text = view.findViewById(R.id.text) as TextView

    text.text = message
    Toast(context).apply {
        setDuration(Toast.LENGTH_SHORT)
        setView(view)
    }.show()
}
```

---

```
Copyright 2020 Imam Mufiid
```