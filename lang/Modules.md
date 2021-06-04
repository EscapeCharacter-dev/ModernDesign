# Modules
This file is about modules.
## What are modules?
Modern Modules are libraries or programs. They are XML files. Sample structure:  
```xml
<Module name="MySuperCoolModule" version="1.0.0">
    <Debug>
        <!--> Debug info goes here. <-->
    </Debug>
    <Symbols>
        <!--> Symbols go here. <-->
        <SymFunction name="MyFunction" type="void">
            <Params>
                <Param name="a" type="int">A does something</Param>
                <Param name="b" type="int">B does something</Param>
            </Params>
            This function does something.
        </SymFunction>
    </Symbols>
    <Code>
        <!--> Here lies an assembly output. <-->
    </Code>
    <Dependencies>
        <!--> Here lies a list of other modules required by this one. <-->
        <Module dependency="true" name="ModernSDK" version="_latest"></Module>
    </Dependencies>
</Module>
```  
Note: Not all compilers will indent the module files.
## How to use them
Modules are like static objects, but they support all platforms and dependencies.  
In your code, you can include a module like so:  
```
using "ModuleName";
```  