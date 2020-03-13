![Networking](https://raw.githubusercontent.com/freshOS/Networking/master/banner.png)

# Networking
[![Language: Swift 5](https://img.shields.io/badge/language-swift5-f48041.svg?style=flat)](https://developer.apple.com/swift)
![Platform: iOS 13+](https://img.shields.io/badge/platform-iOS%2013%2B-blue.svg?style=flat)
[![SPM compatible](https://img.shields.io/badge/SPM-compatible-4BC51D.svg?style=flat)](https://swift.org/package-manager/)
[![License: MIT](http://img.shields.io/badge/license-MIT-lightgrey.svg?style=flat)](https://github.com/freshOS/ws/blob/master/LICENSE)
[![Build Status](https://app.bitrise.io/app/a6d157138f9ee86d/status.svg?token=W7-x9K5U976xiFrI8XqcJw&branch=master)](https://app.bitrise.io/app/a6d157138f9ee86d)
[![codebeat badge](https://codebeat.co/badges/ae5feb24-529d-49fe-9e28-75dfa9e3c35d)](https://codebeat.co/projects/github-com-freshos-networking-master)
![Release version](https://img.shields.io/github/release/freshos/Networking.svg)

[Reason](#why) - [Example](#usage) - [Installation](#installation)

The simplest JSON Networking layer for Swift.  
URLSession + Combine + Generics = Networking.

-
⚠️ Warnign: this is R&amp;D and purely experimental still.
Use at your own risk 👨‍🔬💥
-


### Motive
Networking is the next generation of the [ws](https://github.com/freshOS/ws) project.
The improvements are: Using Combine native Apple's framework over [Then](https://github.com/freshOS/Then) Promise Library, removing [Arrow](https://github.com/freshOS/Arrow) dependency to favour Codable (Arrow can still be adatped easily though) and removing the [Alamofire](https://github.com/Alamofire/Alamofire) dependency in favour of a simpler purely native [URLSession](https://developer.apple.com/documentation/foundation/urlsession) implementation.  
In essence, less dependencies and more native stuff.


====


```swift
let network = NetworkingClient(baseUrl: "http://jsonplaceholder.typicode.com")

network.get("/users").sink(receiveCompletion: { _ in }) { (json:Any) in
    // Get back some json \o/
}.store(in: &cancellables)
```
Because JSON apis are used in **99% of iOS Apps**, this should be  **simple**.  
We developers should **focus on our app logic** rather than *boilerplate code* .  
*Less* code is *better* code
## Try it!

Networking is part of [freshOS](https://freshos.github.io) iOS toolset. Try it in an example App ! <a class="github-button" href="https://github.com/freshOS/StarterProject/archive/master.zip" data-icon="octicon-cloud-download" data-style="mega" aria-label="Download freshOS/StarterProject on GitHub">Download Starter Project</a>

## Why

## How
By providing a lightweight client that **automates boilerplate code everyone has to write**.  
By exposing a **delightfully simple** api to get the job done simply, clearly, quickly.  
Getting swift models from a JSON api is now *a problem of the past*


## What
- [x] Build concise Apis
- [x] Automatically map your models
- [x] Built-in network logger
- [x] Pure Swift, Simple & Lightweight
- [x] Uses Apple's Combine
- [x] 0 Dependencies
