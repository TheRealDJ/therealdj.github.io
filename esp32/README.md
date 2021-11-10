# Install IDF (4.4) and Arduino ESP32 (master) as a component
 - Arduino ESP32 master is tracking IDF v4.4 (since before 2021-11-10)
 - ESP IDF commit id: 6a7d83af1984b93ebaefa7ca9be36304806c3dc8
 - Arduino ESP32 commit id: 16a9cf781fafffedd70b794beed24853965d78ce

```
git clone -b release/v4.4 https://github.com/espressif/esp-idf.git
cd esp-idf/components
git clone https://github.com/espressif/arduino-esp32.git arduino
cd arduino
git submodule update --init --recursive
cd ../..
. export.sh
```

# Install IDF and Arduino ESP32 from commit id
 - Use this if the latest versions don't work together

```
git clone https://github.com/espressif/esp-idf.git
cd esp-idf
git checkout 6a7d83af1984b93ebaefa7ca9be36304806c3dc8
cd components
git clone https://github.com/espressif/arduino-esp32.git arduino
cd arduino
git checkout 16a9cf781fafffedd70b794beed24853965d78ce
git submodule update --init --recursive
cd ../..
./install.sh
```

# Enable IDF
```
cd esp-idf
. export.sh
```
Now you can use the ```idf.py``` command

# Test IDF/Arduino environment
 - I created a template for an Arduino as a component project. The ```sdkconfig``` file may need to be adjusted to fit your project's needs. See [https://github.com/TheRealDJ/esp-idf-arduino-template](https://github.com/TheRealDJ/esp-idf-arduino-template) for details

```
git clone https://github.com/esp-idf-arduino-template
cd esp-idf-arduino-template
idf.py build
```
