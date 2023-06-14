# KeychainClass
Swift simple keychain access class


Usage:

      KeychainInterface.service = "test.com.test"
      KeychainInterface.account = "test.com.apikey"
 
      func doSaveKey(_ theKey: String) {
          // if there is no key, store `theKey` in keychain
          if KeychainInterface.getKey() == nil {
              KeychainInterface.setKey(key: theKey)
          } else {
              // if there is already a key in keychain, must use update to override the old one
              KeychainInterface.updateKey(key: theKey)
          }
      }

