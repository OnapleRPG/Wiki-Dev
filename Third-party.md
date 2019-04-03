# Itemizer thrid party
## Introduction
__Itemizer__ only support Minecraft vanilla feature whereas it implement a third-party system that allow more item customisation. Third-party can build items with more __components__ and __behaviours__. Itemizer will compile all thrid-party data and set it in item [NBT](https://minecraft.gamepedia.com/Tutorials/Command_NBT_tags).
## How to
First, you need to create a _sponge plugin_ with a dependency to __Itemizer__.
* Create a`DataManipulator` who can apply your data to the item.
* Create a `class` who implement `com.onaple.itemizer.data.beans.ItemNbtFactory`
* In there you can set attributes and the mapping for the serialization
* Change Configuration 

> If you want to learn more about DataManipulator follow the sponge [docs](https://docs.spongepowered.org/stable/en/plugin/data/index.html).

### Item Nbt factory
The ItemNbtFactory interface contains all methods you need to implement to create your addon.
```Java
public class EffectFactory implements ItemNbtFactory { 

    @Setting("effects")
    private Map<String, Integer> effects; 

    @Override
    public Key getKey() {
        return HeKeys.HIT_EFFECT;
    }

    @Override
    public DataManipulator<?, ?> constructDataManipulator() {
        return new HitEffectData(effects);
    }
```
1. Implement the interface
2. Get data from configuration
3. Override method `getKey()` with the sponge key
4. Override method `constructDataManipulator()` with your datamanipulator  


### Configuration

```Hocon
nbt=[
            {
                "__class__"="com.onaple.EffectFactory"
                effects {
                    slowness=50
                }
            }
        ]
```
1. open `{}` in the nbt array
2. in the `__class__` node indicate the path to your factory class.
3. put your data 

