# css
cocos2d-x style sheet

a
----
```
css::attribute_set
	* get/set
css::object
	* add/remove class
	* set/get id
		
css::global
```

class
----
```css
.Sprite{
}
.FooMonster{
  image : 'foo.png';
  
  position : 10px, 10px; /* 기본 스폰 위치 */
}
```
```C++
class FooMonster :
	public cocos2d::Sprite,
	public css::object {
public:
  FooMonster()  : 
    klass("FooMonster"){
  }
}
```

id
----
```css
.FooMonster #selected {
  opacity : 0.5; /* 반투명 */
  scale : 1.1;
}
```
```C++
auto foo = FooMonster::create();

foo->id("selected");
```
