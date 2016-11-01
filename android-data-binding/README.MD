## Android Data Binding Adapter

How to make a Android Binding Adapter in Kotlin

```kotlin
// MyBindingAdapter.kt
package com.my.package

import android.databinding.BindingAdapter
import android.widget.LinearLayout

@BindingAdapter("myattr")
fun LinearLayout.anyNameFunc(index: Int) {
	// just do it
}
```

## Usage
```xml
<?xml version="1.0" encoding="utf-8"?>
<layout
	xmlns:android="http://schemas.android.com/apk/res/android"
	xmlns:app="http://schemas.android.com/apk/res-auto">

	<data>

		<variable
			name="position"
			type="int"
		/>
	</data>

	<LinearLayout
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		app:myattr="@{position}"
	>

	</LinearLayout>
</layout>
```
