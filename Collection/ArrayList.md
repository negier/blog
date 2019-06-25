## 一句话
内部就是一个数组elementData，每次添加一个元素，ArrayList就通过Arrays.copyOf方法增加一个元素的容量，在通过elementData[size++] = e添加进去
## 时间复杂度
O(N) 

官方注释：that is, adding n elements requires O(n) time.
## ArrayList扩展数组大小的方法
```
elementData = Arrays.copyOf(elementData, newCapacity);
```
## 官方说这个类和Vector很像，有多像呢
![](https://github.com/negier/blog/blob/master/Pictures/ArrayList_and_Vector.png)
和vector的区别：ArrayList是unsynchronized，其没有处理线程同步
## 用ArrayList创建一个线程同步的List
```
List list = Collections.synchronizedList(new ArrayList(...));
```
