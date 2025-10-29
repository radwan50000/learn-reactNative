# learn-reactNative
## To Reset Your Project Run 

# (First You Must Setup the Nativewind in the project the steps in the pdf)⭐.

> This Will Delete all the code come with the project in first init and return it to be clean to code

```bash

npm run reset-project

```
## To make normal page in app folder -> index.tsx :

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
