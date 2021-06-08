### **Installation**

![Screenshot (187)](https://user-images.githubusercontent.com/62256509/121091097-18b87480-c807-11eb-9aa6-6eedddaf9c20.png)


### **Setting up Windows Environment Variables**

![setup-pytorch](https://user-images.githubusercontent.com/62256509/121090891-dd1daa80-c806-11eb-8c25-17da0f0cffeb.png)


### **Setting up Pytorch-C++ in Microsoft Visual Studio**


**In project properties ------- C/C++ -> General -> Additional Include Directories**

Setting include paths

* C:\Users\91939\Downloads\libtorch-win-shared-with-deps-debug-1.8.1+cpu\libtorch\include
* C:\Users\91939\Downloads\libtorch-win-shared-with-deps-debug-1.8.1+cpu\libtorch\include\torch\csrc\api\include
* C:\Program Files (x86)\Microsoft Visual Studio\Shared\Python37_64\include

**Under Linker -> General -> Additional Library Directories**

Setting lib:

* C:\Users\91939\Downloads\libtorch-win-shared-with-deps-debug-1.8.1+cpu\libtorch\lib
* C:\Program Files (x86)\Microsoft Visual Studio\Shared\Python37_64\libs

**Under Linker -> Input -> Additional Dependencies :**

Add:

torch.lib
torch_cpu.lib
c10.lib
python37.lib

**In C/C++ →Language :**

Change Conformance mode to No. This setting is to prevent some errors [‘std’: ambiguous symbol]

**Build**

Copy all `dll` commands from -- C:\Users\91939\Downloads\libtorch-win-shared-with-deps-debug-1.8.1+cpu\libtorch\lib , to --- x64->Debug


**Reference:**

* https://raminnabati.com/post/004_adv_pytorch_integrating_pytorch_cpp_frontend_in_visual_studio_on_windows/
