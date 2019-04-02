# Itemizer thrid party
## Introduction
Itemizer implement a third-party system that allow more item customisation.
third-party can set data in the item config file and Itemizer will add these to the item nbt data.
## How to Do
follow the steps
* Create a `class` who implement `com.onaple.itemizer.data.beans.ItemNbtFactory`  
* Create a `DataManipulator`  
* Change Configuration 

### Item Nbt factory
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
> If you want to learn more about DataManipulator follow the sponge [docs](https://docs.spongepowered.org/stable/en/plugin/data/index.html).

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

