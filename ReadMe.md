# BrandMessenger:

Development branch of **khoros-android** repo corresponds to release **3.0.1** on Jitpack ( in case of releasing latest version, update development branch from master and make appropriate changes)

**Rocks & Ropes** requires some additional dependencies as we are releasing aar/jars on Jitpack:

    implementation 'com.google.dagger:dagger:2.25.2'
    annotationProcessor 'com.google.dagger:dagger-compiler:2.25.2'
    implementation 'com.squareup.okhttp3:okhttp:3.12.6'
    implementation 'com.davemorrissey.labs:subsampling-scale-image-view:3.10.0'
    implementation 'com.squareup.retrofit2:retrofit:2.6.2'
    implementation 'com.squareup.retrofit2:converter-gson:2.6.2'
    implementation 'com.google.code.gson:gson:2.8.6'
    implementation 'com.github.bumptech.glide:glide:4.9.0'
    implementation 'com.google.android.gms:play-services-location:16.0.0'
    implementation 'com.google.firebase:firebase-messaging:18.0.0'

Dependency to be added for Khoros messaging and core:

    com.github.lithiumtech.brand-messenger-android-sdk:ui:3.0.1
    com.github.lithiumtech.brand-messenger-android-sdk:core:3.0.1


**Auth token to access lib**
You need to generate Auth token on Jitpack and copy that in gradle.properties file
authToken='YOUR_AUTH_TOKEN'

Also, add this in your project's gradle file

    allprojects {
        repositories {
            google()
            jcenter()
            maven {
                url 'https://jitpack.io'
                credentials { username authToken }
            }
        }
    }
