# KeychainClass
Swift simple keychain access class


Usage:
 
      func doSaveKey(_ theKey: String) {
          // if there is no key, store `theKey` in keychain
          if KeyStoreService.getKey() == nil {
              KeyStoreService.setKey(key: theKey)
          } else {
              // if there is already a key in keychain, must use update to override the old one
              KeyStoreService.updateKey(key: theKey)
          }
      }

