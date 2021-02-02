# CopyとCloneの使い分け
## Copy
bitパターンまるっとコピーする

## Clone
型によっては、（アドレスを持つようなもの、Stringとか）まるっとコピーだと、二重freeされちゃうので、`Clone::clone()`を値だけ取り出すように実装する必要がある、

# for用の変数
```rust
    for x in 0..5 {
        handles.push(thread::spawn(move ||{
            println!("Hello, world!: {}", x)
        }));
    }
```

上記でxのmoveが成立しているのは、Loop unrollingにより、各ループで別の変数が割り当てられているとみなしてokだからと推測。
