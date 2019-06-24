# Show-Loader-Library
[![](https://img.shields.io/badge/API-21%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=21#l21)	[![](https://img.shields.io/badge/Platform-Android-brightgreen.svg?style=flat)](https://developer.android.com/about)	[![](https://img.shields.io/badge/Language-Kotlin-brightgreen.svg?style=flat)](https://kotlinlang.org/)	[![](https://img.shields.io/badge/Version-0.1.3-brightgreen.svg?style=flat)](https://git-scm.com/book/en/v1/Getting-Started-About-Version-Control)

An Android library that shows a simple loader.

## Installation

Add the dependency in your `build.gradle`:
```groovy
repositories {
	maven {
		url 'https://jitpack.io' 
	}
}

dependencies {
	implementation 'com.github.SaradarBank:sb-custom-loader:0.1.3'
}
```
Or Maven:
```groovy
<repositories>
	<repository>
		<id>jitpack.io</id>
		<url>https://jitpack.io</url>
	</repository>
</repositories>
<dependency>
	<groupId>com.github.SaradarBank</groupId>
	<artifactId>sb-custom-loader</artifactId>
	<version>0.1.3</version>
</dependency>
```

## Example

1) To show the loader:
```java
val customLoader = CustomLoader()
customLoader.setLoaderMessage("Please Wait")
customLoader.show(supportFragmentManager, "")
```

2) To show the loader with custom tint color:
```java
val customLoader = CustomLoader.newInstance(ContextCompat.getColor(this, R.color.lightestGray))
customLoader.setLoaderMessage("Please Wait")
customLoader.show(supportFragmentManager, "")
```

3) To hide the loader:

```java
customLoader.dismiss()
```
