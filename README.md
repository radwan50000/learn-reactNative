# learn-reactNative
## To Reset Your Project Run 

# (First You Must Setup the Nativewind in the project the steps in the pdf)⭐.

> This Will Delete all the code come with the project in first init and return it to be clean to code

```bash

npm run reset-project

```
## To make normal page with routing in app folder -> index.tsx :

> ``` index.tsx ``` Page

```tsx

import { Text, View } from "react-native";
import {Link} from "expo-router";

export default function Index() {
  return (
    <View className='w-full h-full flex justify-start items-center'>
        <View
            className='w-full h-full flex items-center justify-center'
        >
            <Text>Edit app/index.tsx to edit this screen.</Text>
            <Link
                className='px-8 py-3 bg-gray-400/20 border-2 border-gray-400 mt-4 rounded-md'
                href='/Setting'>
                Setting Page
            </Link>
        </View>
    </View>
  );
}

```

> ``` Setting.tsx ``` Page

```tsx

import React from 'react';
import {View , Text} from 'react-native';

function Setting(){
    return(
        <>
            <View>
                <Text>
                    Setting Page
                </Text>
            </View>
        </>
    )
}

export default Setting;


```


## We can make Dynamic Page Easily with React Native because it use as same as way in the next js in the project 

<ul>
  <li>
    app
  </li>
  <ul>
    <li>
      student
      <ul>
        <li>
          [id].tsx
        </li>
      </ul>
    </li>
    <li>
      index.tsx
    </li>
    <li>
      setting.tsx
    </li>
  </ul>
</ul>



> ``` student/[id].tsx ``` Page

```tsx

import {View, Text} from 'react-native'
import React from 'react'
import {useLocalSearchParams} from "expo-router";

export default function Students() {
    const {id} = useLocalSearchParams();

    return (
        <View>
            <Text>
                Welcome Student : {id}
            </Text>
        </View>
    )
}



```

> ``` index.tsx ``` Page


```tsx

import {Text, View} from "react-native";
import {Link} from "expo-router";

export default function Index() {
    return (
        <View className='w-full h-full flex justify-start items-center'>
            <View
                className='w-full h-full flex items-center justify-center'
            >
                <Text>Edit app/index.tsx to edit this screen.</Text>
                <Link
                    className='px-8 py-3 bg-gray-400/20 border-2 border-gray-400 mt-4 rounded-md'
                    href='/Setting'>
                    Setting Page
                </Link>
                <Link
                    className='px-8 py-3 bg-gray-400/20 border-2 border-gray-400 mt-4 rounded-md'
                    href='/student/Muhammed'>
                    Student Muhammed
                </Link>
            </View>
        </View>
    );
}






```
