函数式接口 | 参数类型 |返回类型 |描述
---|---|---|---
A|B|C|D
SS|无|T|提供一个T类型的值


### 在StreamAPI中使用的函数式接口
函数式接口 | 参数类型 |返回类型 |描述
---|---|---|---
Supplier<T>|无|T|提供一个T类型的值  
Consumer<T> | T |void |处理一个T类型的值  
BiConsumer<T,U> | T, U | void|处理T类型和U类型的值  
Predicate<T>|T|boolean|一个计算Boolean值的函数  
ToIntFunction<T>|T |int |计算int值的函数  
ToLongFunction<T>|T|long|计算long值的函数  
ToDoubleFunction<T>|T|double|计算double的函数  
IntFunction<R>|int|R|参数为int类型的函数(特别注意)  
LongFunction<R>|long|R|参数为long类型的函数  
DoubleFunction<R>|double|R|参数类型为double的函数  
Function<T,R>|T|R|一个参数类型为T的函数  
BiFunction<T,U,R>|T,U|R|一个参数为T和U的函数  
UnaryOperator<T>|T|T|对T进行一元操作  
BinaryOperator<T>|T,T|T|对T进行二元操作  

###  常用的函数式接口
函数式接口 | 参数类型 |返回类型 |抽象方法名|描述|其他方法  
---|---|---|---|---|---
Runnable|无|void|run|执行一个没有参数和返回值的操作|  
Supplier<T>|无|T|get|提供一个T类型的值|  
Consumer<T>|T|void|accept|处理一个T类型的值|chain  
BiConsumer<T,U>|T,U|void|accept|处理T类型和U类型的值|chain  
Function<T,R>|T|R|apply|一个参数类型为T的函数|compose,andThen,identity  
BiFunction<T,U,R>|T,U|R|apply|一个参数类型为T和U的函数值|andThen  
UnaryOperator<T>|T|T|apply|对类型T进行的一元操作|compose,andThen,identity  
BinaryOperator<T>|T,T|T|apply|对类型T进行的二元操作|andThen  
Predicate<T>|T|boolean|test|一个计算boolean值的函数|And,or,negate,isEqual  
BiPredicate<T,U>|T,U|boolean|test|一个含有两个参数,计算boolean的函数|and,or,negate  


