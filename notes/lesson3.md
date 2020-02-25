# lesson 3
- `void` what the function is expected to return
- its not going to return anything
- void = no return value
- you can return it in a way
```
String greeting => 'hellow';
```
which is same as 
```
String greeting() {
    return 'hellow';
}
```
- list is same is like an array
```
void main() {
    List names = ['jin', 'mochi', 'ally'];
    print(names);
    }
```

- you canadd by using `names.add('jin');`
- you can remove by using `names.remove('jin')`
- names.add(30) will work. However, its good to say what kinda data is going to be in the list
```
List<string> names = [only will take in string];
```

## Classes
- blueprint for object
- like user object like age, name
- like shopping cart object
```
class User {

    String username = 'jin';
    int age = 31; 

    //can create function
    void login() {
        print('user logged in');
    }
}/// this is printing///

```
- when you call it its call instantiating and it will be stored
- you can save it by assigning variable.
    - invoke it like `username(the name of the variable name).age(class variable);
- you can create constructor to not hard code things in the class
```
class User {

    String username;
    int age; 

    user(String username, int age) {
        this.username = username;
        this.age = age;
    };

    //can create function
    then invoke it by 
User('jin', 31)

```
### inheritance
- superuser to inherit everything and also have extra function
- not normal user to have this authority

```
class SuperUser extends user {

    SuperUser(String username, int age) : super(username, age);
    ///

    void publish() {
        print('published update')
    }

}
//// invoke it by
SuperUser userThree = SuperUser('Yoshi', 20);
print(userThree.username);
userThree.publish();

// userTwo or other user doesn't have access to the publish

```