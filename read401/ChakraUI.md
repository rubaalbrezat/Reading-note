# Chakra UI

## What is a Chakra UI?
Chakra UI is a simple, modular and accessible component library that gives you the building blocks you need to build your React applications.

## Is Chakra UI better than material UI?

Chakra UI is a more robust, layout-focused library that also provides developers with UI components similar to those that Material UI provides, but has a greater focus on the creation of flexible, composable, and scalable code. A core concept to be considered when comparing the two frameworks is 'Ease of Modification'

## How to use Chakra UI?
 using npm

npx create-react-app my-app --template [template-name]

 Installation

npm i @chakra-ui/react @emotion/react@^11 @emotion/styled@^11 framer-motion@^6

Provider Setup

import * as React from 'react'

// 1. import `ChakraProvider` component
import { ChakraProvider } from '@chakra-ui/react'

function App() {
  // 2. Wrap ChakraProvider at the root of your app
  return (
    <ChakraProvider>
      <App />
    </ChakraProvider>
  )
}