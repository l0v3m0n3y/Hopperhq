# Hopperhq
api for Hopperhq.com funny userfull tools site
# main
```cpp
#include "Hopperhq.h"
#include <iostream>

int main() {
   Hopperhq api;

    auto username = api.username_checker("instagram","username").then([](json::value result) {
        std::cout << "Search results: " << result.serialize() << std::endl;
    });
    username.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
