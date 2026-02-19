# Syntax Highlighting on Wasm
Date: 2026-02-19
Tags: wasm, markdown, ui
Summary: A quick check that fenced code blocks render with syntax colors in the post window.

This post is only for visual verification of markdown code highlighting.

## Rust Example

```rust
#[derive(Debug)]
struct DraftPost {
    title: String,
    tags: Vec<String>,
}

impl DraftPost {
    fn slug(&self) -> String {
        self.title.to_lowercase().replace(' ', "-")
    }
}

fn main() {
    let post = DraftPost {
        title: "Syntax Highlighting on Wasm".to_owned(),
        tags: vec!["wasm".into(), "markdown".into()],
    };
    println!("slug = {}", post.slug());
}
```

## JavaScript Example

```js
async function loadManifest() {
  const response = await fetch("/content/posts/manifest.json");
  if (!response.ok) throw new Error(`HTTP ${response.status}`);
  const manifest = await response.json();
  return manifest.posts.map((post) => post.title);
}
```

## C++ Example

```cpp
#include <iostream>
#include <string>
#include <vector>

int main() {
    std::vector<std::string> tags = {"wasm", "markdown", "cpp"};
    std::cout << "tags:";
    for (const auto& tag : tags) {
        std::cout << " #" << tag;
    }
    std::cout << std::endl;
    return 0;
}
```

## Go Example

```go
package main

import "fmt"

func main() {
    tags := []string{"wasm", "markdown", "go"}
    fmt.Printf("tags: %v\n", tags)
}
```

## TOML Example

```toml
[features]
web_app = ["http", "persistence"]
http = ["ehttp", "egui_extras/http", "egui_extras/image"]
```
