#Bachelor #Informatik #ConPra 
# Rust
```Rust
fn union (a : i32, b : i32, mut parent : &mut Vec<i32>, size : &mut Vec<i32>) -> i32 {
    let mut root_a = find(a, &mut parent);
    let mut root_b = find(b, &mut parent);

    if root_a == root_b {
        return root_a;
    }

    if size[root_a as usize] < size[root_b as usize] {
        let temp = root_a;
        root_a = root_b;
        root_b = temp;
    }

    parent[root_b as usize] = root_a;
    size[root_a as usize] = size[root_a as usize] + size[root_b as usize];
    return root_a;
}

fn find (a : i32, parent : &mut Vec<i32>) -> i32 {
    let mut root = a;
    loop {
        if parent[root as usize] == root {
            break;
        }
        root = parent[root as usize];
    }

    let mut current = a;
    while current != root {
        let next_elem = parent[current as usize];
        parent[current as usize] = root;
        current = next_elem;
    }

    return root;
}
```
