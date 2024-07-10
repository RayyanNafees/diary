---
icon: LiDatabase
---

## More Performant & Scalable

a Rust's Actix-Web/yew/Leptos/Axum based pocketbase alternative with better performance than go's Pocketbase

Or just Pocketbase but using a faster and better framework like Go-Fiber or Fast-HTTP and gopher.js on frontend

Or just like Astro's compiler - A WASM based pocketbase alternative 
Or anything that just beats pocketbase in performance and scalability

## Streaming & Sync with Cloud, Branches, Version Control

Provides features like Lite-Stream & Turso Sync, S3 buckets, Auth using goth / go-true etcetera

## Extensible Features with SQLpkg

And all the features of SQL at its peak using [sqlpkg](https://sqlpkg.org/all/)

## Performance & Scalability impact metrics

For performance reasons make them to be turned off or on for the project and carefully benchmark the bottlenecks and edge-cases or The impact they have on performance, memory/CPU consumption & Scalability

### AI

U can turn sql extensions (installed via sqlpkg) on or off, and based on the changes u did after u turned on and used the extensions, ai goes through all of it and tells u what changes should be done once u turn off (and remove) the extension from the database (or does all operations for u and asks your permission to accept the changes to the effected files, or review them yourself)

Can also suggest things to do to improve performance & scalabilty andefficiency of the database queries

Also suggest indices based on the search data logs

Also acts as autocompletes when typing stuff up

Can generate ERDiagrams in mermaid.js and suggest better Entity Relations for efficiency, performance & scalabilty 

## DuckDB

Easily portable to DuckDB & can aslo be used with its extensions 

> Try coverting all the sqlpkg to duckdb - that way u will be able to master duckdb as well
> or create a `dpkg` as  a fork of `sqlpkg` that installs duckdb extensions