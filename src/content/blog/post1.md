---
title: "Diving into Rust: A beginner's journal | part 1"
description: "My learning journey on rust"
pubDate: "Aug 27 2023"
heroImage: "/rust"
tags: ["Rust"]
---

Welcome to my rust programming journey! I'm new to the world of Rust and decided to share my learning process through this blog. My approach is all about simplicity - breaking down Rust concepts into easily digestible pieces.

### Why this blog?

Learning Rust is my main goal, but I'm not doing it alone. I'm inviting you to join me. If you're experienced in rust, your feedback and guidance would be invaluable. Let's learn together and build a supportive community.

### Simplicity

Complex topics won't deter me. I believe in learning by doing and explaining things in the simplest way possible. This blog is a collection or a repository of sorts and I'll try to be as simple as possible with my explanations. I'll be quite verbose with my explanation of some topics and may use analogies to explain certain topics.

### Table of contents:

1. What is Rust?
    
2. Why Rust?
    
3. Installing Rust:
    
    * Windows
        
    * Mac OS and Linux
        

### **What is rust?**

Before we dive into the installation process, let's briefly discuss what Rust is.

Rust is a modern programming language known for its emphasis on memory, safety, performance and concurrency. It's a great choice for building systems, applications and more.

### Why Rust?

Before we start coding in Rust. It's important to understand why it's worth your time. Rust's unique features, such as its ownership system and borrow checker, help prevent common programming errors like null pointers and data races. This results in more reliable and secure code. In Rust, the compiler plays a gatekeeper role by refusing to compile code with these difficult-to-find bugs.

You may wonder what is ownership system and borrow checker are. We will discuss these topics in depth in further parts for the time being. I'll have a quick explanation regarding topics as it is crucial to know about them.

#### Null pointers

Null pointers are pointers that point to nothing as their value is NULL( 0 ). It is used to represent the absence of a valid value or reference in a variable or memory location. Think of it as an empty container with no label you're not sure what's supposed to be inside.

However, null pointers are troublemakers. When code encounters them unexpectedly, it can lead to crashes or errors. It's like trying to use a tool you thought was in your toolbox, only to realize it's not there when you need it.

Rust, a modern programming language, tackles this issue with finesse. Instead of relying on null pointers, Rust uses the "Option" type. It's like having a special box that's either empty ("None") or contains something ("Some"). This way, Rust forces programmers to always consider both possibilities, preventing surprises and making code safer.

#### Data races

A data race is a type of concurrency bug that occurs when multiple threads access shared data concurrently, at least one of the accesses is a write operation, and there's no synchronization mechanism in place to control the order of these accesses. In other words, data races happen when threads interact with shared data in a way that leads to unpredictable and incorrect behavior.

Data races can be incredibly challenging to debug because they often result in sporadic and unpredictable errors that are hard to reproduce consistently. These errors can lead to crashes, corrupted data, and unexpected program behavior.

**Why Rust Is Preferred for Preventing Data Races:**

Rust takes a unique approach to prevent data races and ensure memory safety in concurrent programming. Here's why Rust stands out in this regard:

1. **Ownership and Borrowing:** Rust's ownership and borrowing system enforces strict rules about how data can be accessed and modified. It ensures that only one thread can have mutable access to data at any given time. This prevents data races by design, as the compiler checks and enforces these rules at compile time.
    
2. **No Implicit Sharing:** In Rust, data is not shared between threads implicitly. Instead, data can be explicitly shared using mechanisms like `Arc` (atomic reference counting) and locks. This forces developers to be intentional about sharing and synchronizing data.
    
3. **Concurrency Primitives:** Rust provides powerful concurrency primitives like `Mutex`, `RwLock`, and channels that help manage access to shared data. These primitives ensure that only one thread can access the data at a time, preventing data races.
    
4. **Thread Safety in the Type System:** Rust's type system enforces thread safety rules. Types like `Send` and `Sync` indicates whether a type can be safely sent between threads or accessed concurrently. The compiler ensures that types that aren't `Send` or `Sync` cannot be used in concurrent contexts.
    
5. **Fearless Concurrency:** Rust's approach to preventing data races shifts the burden of responsibility from runtime debugging to compile-time analysis. This means that developers can have confidence in their code's correctness even in the presence of concurrency.
    

Programming in Rust is like having a helpful friend who won't lend you their tools unless you promise not to break them. It's like they're saying, 'I'll let you use my wrench, but only if you promise not to turn it into a spaghetti fork!' That's why Rust is the language of responsible coding – it's all about preventing surprise disappearances and turning tools into dinnerware.

Wow, that was quite the Rust explanation! It turned out longer than waiting for a Windows update.

### Install rust

For the installation, I'll primarily discuss installing Rust in Unix and Linux-based distributions as i primarily use pop OS as my daily driver.

My preferred method of installing rust is using a tool called `rustup`. Open the terminal and run this command below.

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

once that's done run `rustup update` as rust receives updates very frequently. This will ensure your rust installation is up to date.

As for Windows folks. I found a neat [article](www.alpharithms.com/installing-rust-on-windows-403718) that explains how to install rust on windows.

Thanks for joining me on this Rust journey! I aimed for simplicity in explaining complex topics. Whether you're new to Rust or experienced, your feedback is gold. If you spotted any hiccups in my explanations or want to share your thoughts, please don't hesitate.