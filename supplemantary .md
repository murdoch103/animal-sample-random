```python
import random
```


```python
goats = ["goat1", "goat2", "goat3", "goat4", "goat5", "goat6", "goat7", "goat8", "goat9", "goat10", "goat11", "goat12", "goat13", "goat14", "goat15", 
        "goat16", "goat17", "goat18", "goat19", "goat20", "goat21", "goat22", "goat23", "goat24"]
```


```python
num_groups = 3
```


```python
random.shuffle(goats)
```


```python
goats_per_group = len(goats)//num_groups
```


```python
groups = [goats[i:i + goats_per_group] for i in range(0, len(goats), goats_per_group)]
```


```python
remaining_goats = len(goats) % num_groups
for i in range(remaining_goats):
    groups[i].append(goats[-(i+1)])
```


```python
group_names = ["Control", "SARA", "CBM"]
```


```python
for idx, group in enumerate(groups):
    print(f"{group_names[idx]} group: {group}")
```

    Control group: ['goat4', 'goat18', 'goat21', 'goat13', 'goat16', 'goat1', 'goat9', 'goat17']
    SARA group: ['goat6', 'goat8', 'goat24', 'goat11', 'goat14', 'goat3', 'goat19', 'goat15']
    CBM group: ['goat12', 'goat20', 'goat5', 'goat2', 'goat10', 'goat7', 'goat23', 'goat22']



```python

```
