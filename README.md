Buffer Text Input Layout
-------------------------

~~(Coming to maven central soon!)~~
Now available on Gradle. Check [**Installation**](https://github.com/wajahatkarim3/BufferTextInputLayout#installation) section.

This is a simple customisation of the TextInputLayout found in the Design Support Library.

Whilst this is an awesome component that we've made great use of, we wanted to be able to display
the counter so that the value displayed was:

- Not formatted in the way that the support library version was
- Only visible when we reach a certain number of characters away from the maximum counter value

Hence why we created this simple component :)

## Ascending

![Ascending](/art/ascending.gif)

## Descending

![Descending](/art/descending.gif)

## Standard

![Standard](/art/standard.gif)


## Display when a given count away from the maximum value

![Hidden](/art/hidden.gif)

# Installation

## Gradle
```groovy
compile 'com.wajahatkarim3.BufferTextInputLayout:buffertextinputlayout:1.2.0'
```

## Maven
```
<dependency>
  <groupId>com.wajahatkarim3.BufferTextInputLayout</groupId>
  <artifactId>buffertextinputlayout</artifactId>
  <version>1.2.0</version>
  <type>pom</type>
</dependency>
```

# How to use

In exactly the same way as the support library! Simply wrap an edit text field like so:

```xml
<org.buffer.android.buffertextinputlayout.BufferTextInputLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:counterEnabled="true"
        app:counterMaxLength="10"
        app:counterOverflowTextAppearance="@style/counterOverride"
        app:counterTextAppearance="@style/counterText"
        app:hintEnabled="true"
        app:counterMode="ascending">

    <EditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="@string/text_hint" />

</org.buffer.android.buffertextinputlayout.BufferTextInputLayout>
```

# Setting attributes via XML

In our XML layout, we can set two extra attributes for the BufferTextInputLayout:

- app:counterMode -> Set the mode in which the counter should use when being displayed (DESCENDING, ASCENDING, STANDARD)
- app:displayFromCount -> Set the value for which how many characters should be remaining until the counter becomes visible

e.g

```xml
app:displayFromCount="5"
app:counterMode="descending"
```


# Setting attributes programmatically

- setCounterMode(CounterMode counterMode) -> Set the mode in which the counter should use when being displayed (DESCENDING, ASCENDING, STANDARD)
- setCharactersRemainingUntilCounterDisplay(int remainingCharacters) -> Set the value for which how many characters should be remaining until the counter becomes visible

e.g.
```java
bufferTextInputLayout.setCounterMode(CounterMode.DESCENDING);
bufferTextInputLayout.setCharactersRemainingUntilCounterDisplay(40);
```

# Developed By
This component has been completely developer by team at [Buffer](https://github.com/bufferapp) and has been forked from their [BufferTextInputLayout](https://github.com/bufferapp/BufferTextInputLayout) library. I have only uploaded the AAR on jCenter() and Maven() so that other developers can use it directly using gradle.

# License

    Copyright 2018 Wajahat Karim

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
