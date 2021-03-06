
⚠️ The [Arduino SDK](https://github.com/parse-community/Parse-SDK-Android/tree/1.20.0) has been retired due to a lack of contribution and use. If you intent to continue using this SDK you can still fork the repo. If you are interested in maintaining it please make yourself known and we would be happy to unarchive it.

-----

# Getting Started

If you haven't installed the SDK yet, please [head over to the Arduino SDK repository](https://github.com/parse-community/Parse-SDK-Arduino) to install the SDK in the Arduino IDE. Note that this SDK requires the Arduino Yún and the Arduino IDE v1.6.0+.

The Parse platform provides a complete backend solution for your hardware device. Our goal is to totally eliminate the need for writing server code or maintaining servers.

Note that the Arduino SDK only contains a subset of Parse features found in mobile and desktop. This allows the SDK to be smaller in size and more performant, making it suitable for constrained embedded environments. The Arduino SDK is fully open source, and anyone can contribute to make it better, or make their own changes if necessary. Check out the [GitHub repository](https://github.com/parse-community/parse-embedded-sdks) for more information.

## Initialization

In order for Parse to know which app is associated with the Arduino device, simply specify the application ID and client key in your `setup` function:

```cpp
void setup() {
	Parse.begin("${APPLICATION_ID}", "${CLIENT_KEY}");
	// ...
}
```

After this, all calls to the Parse Server will use the specified app.
