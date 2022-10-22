## Table of Contents

- [CPP STL CheatSheet for Developers](#cpp-stl-cheatsheet-for-developers)
	- [Vector](#vector)
		- [Vector insertion](#vector)
		- [Vector Display](#vector)
		- [Vector Maximum element](#vector)
		- [Vector Minimum element](#vector)
		- [Vector sort](#vector)
		- [Vector reverse](#vector)
		- [Vector deletion](#vector)
	- [Set](#set)
		- [Set insertion](#set)
		- [Set Display](#set)
	- [Unordered Set](#unordered-set)
		- [Unordered insertion](#unordered-set)
		- [Unordered Display](#unordered-set)
	- [Map](#map)
		- [Map insertion](#map)
		- [Map Display](#map)
	- [Stack](#stack)
		- [Stack insertion](#stack)
		- [Stack Display](#stack)
	- [Queue](#queue)
		- [Queue insertion](#queue)
		- [Queue Display](#queue)
	- [Deque](#deque)
		- [DeQue insertion](#deque)
		- [DeQue Display](#deque)
    - [Vector pair](#vector-pair)
		- [Vector pair insertion](#vector-pair)
		- [Vector pair Display](#vector-pair)


# C++ STL CheatSheet for Developers


### vector

```cpp
    vector<int> v;
    cout << "Insertion of element in vector: " << endl;
    cout << endl;

    for (int i = 0; i < n; i++)
    {
        v.push_back(a[i]);
    }
    cout << "Display element of vector " << endl;

    for (int i = 0; i < n; i++)
    {
        cout << v[i] << " ";
    }
    cout << endl;

    int maximum = *max_element(v.begin(), v.end());
    int minimum = *min_element(v.begin(), v.end());

    cout << "Maximum element in vector " << maximum << endl;
    cout << "Minmum element in vector " << minimum << endl;
    sort(v.begin(), v.end());

    cout << "Sort element of vector " << endl;
    for (int i = 0; i < n; i++)
    {
        cout << v[i] << " ";
    }
    reverse(v.begin(), v.end());
    cout << endl;

    cout << "Reverse element of vector " << minimum << endl;
    for (int i = 0; i < n; i++)
    {
        cout << v[i] << " ";
    }
    cout << endl;

    cout << "Delete last element of vector " << endl;
    v.pop_back();
    for (int i = 0; i < n; i++)
    {
        cout << v[i] << " ";
    }
```

**[🔼Back to Top](#table-of-contents)**

### set

```cpp
	set<int> s;
    cout << endl;

    cout << "Insertion in set " << endl;
    cout << endl;

    for (int i = 0; i < n; i++)
    {
        s.insert(a[i]);
    }
    cout << "Display of set element" << endl;

    for (auto i = s.begin(); i != s.end(); i++)
    {
        cout << *i << " ";
    }
  

```

**[🔼Back to Top](#table-of-contents)**

### unordered-set

```cpp
unordered_set<int> s1;
    cout << endl;

    cout << "Insertion in unordered set " << endl;

    for (int i = 0; i < n; i++)
    {
        s1.insert(a[i]);
    }

    cout << "Display of unordered set element" << endl;

    for (auto i = s1.begin(); i != s1.end(); i++)
    {
        cout << *i << " ";
    }

```

**[🔼Back to Top](#table-of-contents)**


### map

```cpp
map<int, int> m;
    cout << endl;

    cout << "Insertion in map " << endl;
    for (int i = 0; i < n; i++)
    {
        m[a[i]]++;
    }
    cout << "Display of map element" << endl;

    for (auto i = m.begin(); i != m.end(); i++)
    {
        cout << i->first << " " << i->second << endl;
    }  
```

**[🔼Back to Top](#table-of-contents)**

### Stack 

```cpp
    stack<int> st;
    cout << endl;

    cout << "Insertion in stack " << endl;

    for (int i = 0; i < n; i++)
    {
        st.push(a[i]);
    }
    cout << "Display and removal of stack element" << endl;

    for (auto i = s.begin(); i != s.end(); i++)
    {
        cout << st.top() << " ";
        st.pop();
    } 
```

**[🔼Back to Top](#table-of-contents)**

### queue

```queue
	queue<int> q;
    cout << endl;

    cout << "Insertion in queue " << endl;

    for (int i = 0; i < n; i++)
    {
        q.push(a[i]);
    }
    cout << "Display of queue element" << endl;

    for (auto i = s.begin(); i != s.end(); i++)
    {
        cout << q.front() << " ";
        q.pop();
    }
```

**[🔼Back to Top](#table-of-contents)**

### deque

```deque
   deque<int> d;
    cout << "Insertion in deqeue " << endl;

    for (int i = 0; i < n; i++)
    {
        d.push_front(a[i]);
    }
    cout << "Display of dequeue element" << endl;

    for (auto i = s.begin(); i != s.end(); i++)
    {
        cout << d.front() << " ";
        d.pop_back();
    }
    cout << "Deletion of dequeue element" << endl;

    d.pop_back(); 
```

**[🔼Back to Top](#table-of-contents)**

### vector-pair

```cpp
    vector<pair<int, int>> p;
    cout << "Insertion in vector pair " << endl;
    cout << endl;

    for (int i = 0; i < n; i++)
    {
        p.push_back({a[i], i});
    }
    cout << "Display of vector pair element" << endl;

    for (auto i = 0; i < v.size(); i++)
    {
        cout << p[i].first << " " << p[i].second << endl;
    }
    cout << endl;
```
**[🔼Back to Top](#table-of-contents)**

### Contributed By : Khushpreet Singh

**[🔼Back to Top](#table-of-contents)**

