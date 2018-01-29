# All Aboard!

[![Build Status](https://travis-ci.com/tylerbwong/AllAboard.svg?token=AABXGtYrzS4uRtMAUqq3&branch=master)](https://travis-ci.com/tylerbwong/AllAboard)

Create onboarding flows for your app using a clean and simple Kotlin DSL.

# Basic Usage

```kotlin
onboarding {
    backgroundColor = R.color.colorPrimary
    showIndicator = true
    
    // Specify contents with resource ids or strings
    page {
        imageRes = R.drawable.page_one_image
        titleRes = R.string.page_one_title
        subTitleText = "This is a subtitle."
    }

    page {
        imageUrl = "https://images.com/page_two.png"
        titleText = "This is a train."
        subTitleRes = R.string.page_two_subtitle
    }

    page {
        customView = pageThreeView // Use inflated custom views
    }

    page {
        customViewRes = R.layout.page_four // Or just pass a layout resource id!
    }

    onFinish {
        finish()
    }
}
```

# License

    Copyright 2018 Tyler Wong

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
    