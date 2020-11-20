# Custom Toast

- Kotlin
```kotlin
fun customToast(context: Context?, message: String?) {
    val layoutInflater =
        context?.getSystemService(Context.LAYOUT_INFLATER_SERVICE) as LayoutInflater
    val view = layoutInflater.inflate(R.layout.custom_toast, null)
    val text = view.findViewById(R.id.text) as TextView

    text.text = message
    Toast(context, message, Toast.LENTH_SHORT).show()
}
```

---

```
Copyright 2020 Imam Mufiid
```