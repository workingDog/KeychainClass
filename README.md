# KeychainClass
Swift simple keychain access class


Usage:
 
      func doSaveKey(_ theKey: String) {
          if KeyStoreService.getKey() == nil {
              KeyStoreService.setKey(key: theKey)
          } else {
              KeyStoreService.updateKey(key: theKey)
          }
      }

