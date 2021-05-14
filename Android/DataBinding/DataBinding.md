# DataBinding :grapes:

데이터 바인딩 기초 사용법을 정리한 문서입니다.

<br>

### 1. 기초 라이브러리 셋팅

- **build.gradle(app)**

  ```kotlin
  android {
      ...
      buildFeatures {
          dataBinding true
      }
  }
  ```

<br>

### 2. DataBinding Layout

```xml
<layout xmlns:android="http://schemas.android.com/apk/res/android"
            xmlns:app="http://schemas.android.com/apk/res-auto">
        <data>
            <variable
                name="viewmodel"
                type="com.myapp.data.ViewModel" />
        </data>
        <ConstraintLayout... /> <!-- UI layout's root element -->
    </layout>
```

<br>

