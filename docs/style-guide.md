# Style Guide

Unreal Engine has a particular convention for naming files, variables, and functions. This style guide is a reference for the naming conventions used in this project. To be sure, you're reading the spark notes version of the official Unreal Engine Style Guide. Please skip to [#Conclusion](#conclusion) for links to sources.
## Copyright Notice

Make sure all source files have the following notice at the top of the file:

```cpp
    // Copyright Team CGC. All Rights Reserved.
```
It must match the exact format above.

## Naming Conventions  

### General Rules

Make sure that all names start with a capital letter. No underscores between words.

**Correct**:

```cpp
    int MyVariable;
    class MyClass;
```

**Incorrect**:
```cpp
    int myVariable;
    class my_class;
    class myClass;
```

### Boolean Variables

Though an initial capital letter is usually fine, boolean variables specifically diverge a bit from this rule. All booleans should start with "b" and then have an initial capital letter.

**Correct**:

```cpp
    bool bIsTrue;
```

**Incorrect**:

```cpp
    bool IsTrue;
```

### Classes

Unreal Engine has certain conventions for certain types of asset classes. Objects, Actors, Widgets, and Interfaces require a prefix to their name.

**Generalized Example**

```cpp
    class UMyObject;
    class AMyActor;
    class UMyWidget;
    class IMyInterface;
```

Objects should always start with a "U", Actors with an "A", Widgets with a "U", and Interfaces with an "I". Other classes should start with "F".

### Typedefs

Typedefs are denominations given to a type to make it easier to read and understand. Typedefs should start with an "F" if they are a struct or a "U" if they are an object.

### Names and Grammar

Names should be descriptive and follow the rules of the English language. For example, a variable that holds the value of a player's health should be named "PlayerHealth" and not "PercentageValue", as a simple example.

Types and variables should also be nouns, and method names should be verbs that describe the action they perform.

**Correct**:

```cpp
    int PlayerHealth; // A variable that holds the player's health.
    void UpdateHealth(); // A method that updates the player's health.
```

**Incorrect**:

```cpp
    int PercentageValue; // A bad example of a variable that holds the player's health.
    void Health(); // A bad example of a method that updates the player's health.
```

### Booleans

All booleans should be named as though it were a question.

**Examples**
    
```cpp
    bool bIsTrue; // A boolean that asks if something is true.
    bool bIsDead; // A boolean that asks if something is dead.
```

## Assets

Naming conventions for assets are a bit different from the naming conventions for code. Assets should be named in a way that makes them easy to find and understand. Unreal suggests the following convention for naming files:

```bash
[AssetTypePrefix]_[AssetName]_[Descriptor]_[OptionalVariantLetterOrNumber]
```

- **AssetTypePrefix**: A prefix that indicates the type of asset. For example, "SM" for a static mesh, "T" for a texture, "M" for a material, and so on.
- **AssetName**: A descriptive name for the asset. For example, "Wall", "Floor", "Player", and so on.
- **Descriptor**: A descriptor that describes the asset. For example, whether "a texture is a normal map or an opacity map".
- **OptionalVariantLetterOrNumber**: An optional letter or number that distinguishes the asset from other assets of the same type.

**Examples**

```bash
SM_Wall_01
T_Wall_Normal
M_Wall_Brick
```

For a full list of recommended prefixes, please refer to the [Recommended Asset Naming Conventions](https://docs.unrealengine.com/4.27/en-US/ProductionPipelines/AssetNaming/).

## Conclusion

Following the style guide is essential to maintain consistency in the project and ensures that other contributors can easily understand the code. Outlined above is a brief overview and in no means exhaustive, but will likely be expanded upon should the need arise. For a more detailed guide, please refer to the [Unreal Engine Style Guide](https://docs.unrealengine.com/4.27/en-US/ProductionPipelines/DevelopmentSetup/CodingStandard/).
