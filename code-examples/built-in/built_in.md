# Built-In Functions and Global Methods Reference

This document covers all globally available functions and objects registered by the runtime evaluator, grouped by their primary purpose.

---

## 1. Core Utilities

### `len(arg)`

Returns the length of a string or array, or the number of top-level keys in an object.

* **Usage:**
```lopo
len("hello");     # Returns 5
len([1, 2, 3]);   # Returns 3
len({a: 1, b: 2}); # Returns 2

```



### `type(arg)` / `typeOf(arg)`

Determines the raw type of a given value. `typeOf` specifically handles `null` values more gracefully.

* **Usage:**
```lopo
type([1, 2]);     # Returns "array"
typeOf(null);     # Returns "null"

```



### `isEmpty(arg)`

Checks whether a string, array, or object has no content or elements.

* **Usage:**
```lopo
isEmpty("");      # Returns true
isEmpty({});      # Returns true

```



### `clone(arg)` / `deepClone(arg)`

Duplicates data structures. `clone` creates a shallow copy (top-level properties), while `deepClone` creates an independent deep copy of objects or arrays.

* **Usage:**
```lopo
define copy = clone(originalArray);    # items
define freshObj = deepClone(nestedDataStructures); # items

```



### `uuid()`

Generates a random v4-compliant unique identifier string.

* **Usage:**
```lopo
define uniqueId = uuid(); # e.g., "3b234a21-4321-4def-b123-123456789abc"

```



---

## 2. String Formatting & Manipulation

### `str(arg)` / `toStr(arg)`

Converts any incoming raw value directly into a string representation.

* **Usage:**
```lopo
str(100);         # Returns "100"

```



### `lower(str)` / `upper(str)`

Transforms casing styles safely to lower or upper case letters.

* **Usage:**
```lopo
lower("HELLO");   # Returns "hello"
upper("world");   # Returns "WORLD"

```



### `trim(str)` / `trimStart(str)` / `trimEnd(str)`

Removes leading and trailing white spaces.

* **Usage:**
```lopo
trim("  hello  "); # Returns "hello"

```



### `startsWith(str, prefix)` / `endsWith(str, suffix)` / `includes(str, substr)`

Performs character sequence tests inside a target string string. Returns a boolean.

* **Usage:**
```lopo
startsWith("lopo.org", "lopo"); # Returns true
includes("automation", "mat");   # Returns true

```



### `split(str, separator)` / `join(arr, separator)`

Converts strings to arrays or vice versa using delimiter characters.

* **Usage:**
```lopo
split("a,b,c", ","); # Returns ["a", "b", "c"]
join(["x", "y"], "-"); # Returns "x-y"

```



### `substring(str, start, end)`

Extracts a section of a string starting from a index range.

* **Usage:**
```lopo
substring("abcdef", 1, 4); # Returns "bcd"

```



### `replace(str, search, replacement)`

Finds and completely switches specific sections of matching text patterns.

* **Usage:**
```lopo
replace("cat cat", "cat", "dog"); # Returns "dog dog"

```



### `capitalize(str)`

Converts the very first letter of a text string to upper-case layout.

* **Usage:**
```lopo
capitalize("lopo"); # Returns "Lopo"

```



### `reverseStr(str)`

Reverses string sequencing ordering.

* **Usage:**
```lopo
reverseStr("abc"); # Returns "cba"

```



### `padStart(str, length, pad)` / `padEnd(str, length, pad)`

Pads strings with characters to ensure specific length structures are reached.

* **Usage:**
```lopo
padStart("5", 3, "0"); # Returns "005"

```



### `camelCase(str)` / `kebabCase(str)`

Utility converters formatting text phrasing syntax directly.

* **Usage:**
```lopo
camelCase("hello_world"); # Returns "helloWorld"
kebabCase("helloWorld");   # Returns "hello-world"

```



---

## 3. Mathematical Operations

### `num(arg)`

Enforces number structures out of mixed type parameters. Non-numeric structures fall back safely to `0`.

* **Usage:**
```lopo
num("42");        # Returns 42
num("invalid");   # Returns 0

```



### `isNaN(arg)`

Validates whether a target type structure evaluates as an invalid numeric format.

* **Usage:**
```lopo
isNaN("text");    # Returns true

```



### `floor(arg)` / `ceil(arg)` / `round(arg)` / `abs(arg)`

Standard mathematical alignment rules mapping calculations towards integers or positive fields.

* **Usage:**
```lopo
floor(4.9);       # Returns 4
abs(-10);         # Returns 10

```



### `sqrt(arg)` / `pow(base, exp)`

Calculates exponents and mathematical square roots.

* **Usage:**
```lopo
pow(2, 3);        # Returns 8

```



### `min(...args)` / `max(...args)`

Extracts minimum or maximum values out of dynamic numerical arguments fields.

* **Usage:**
```lopo
max(10, 20, 5);   # Returns 20

```



### `clamp(value, min, max)`

Restricts any incoming values safely within lower and upper bounding values.

* **Usage:**
```lopo
clamp(50, 0, 10); # Returns 10

```



### `random(min, max)` / `randomInt(min, max)` / `randomFloat(min, max)`

Creates random numbers across assigned bounding scales.

* **Usage:**
```lopo
randomInt(1, 10); # Returns structural integer between 1 and 10 inclusive

```



### `lerp(a, b, t)`

Linear interpolation tracking algorithm.

* **Usage:**
```lopo
lerp(0, 100, 0.5); # Returns 50

```



### `degToRad(deg)` / `radToDeg(rad)`

Angle converters balancing trigonometric formatting layout configurations.

---

## 4. Array Processing

### `push(arr, val)` / `pop(arr)` / `shift(arr)` / `unshift(arr, val)`

Standard stack operations modifying target array memory elements directly.

* **Usage:**
```lopo
define items = [1, 2];
push(items, 3);    # items becomes [1, 2, 3]

```



### `indexOf(arr, val)` / `includesArr(arr, val)`

Locates or checks element matching inside dynamic storage fields.

* **Usage:**
```lopo
indexOf(["a", "b"], "b"); # Returns 1

```



### `range(start, end, step)`

Generates sequential structural arrays containing numerical series ranges.

* **Usage:**
```lopo
range(0, 5);      # Returns [0, 1, 2, 3, 4]

```



### `map(arr, fn)` / `filter(arr, fn)` / `reduce(arr, fn, initial)`

Functional array processing utilities that run asynchronously.

* **Usage:**
```lopo
define doubled = await map([1, 2], func(x) { return x * 2 });

```



### `sort(arr, fn)` / `reverse(arr)`

Reorders structural sequencing properties directly in place.

### `flatten(arr)`

Flattens deeply nested structural elements continuously down down into single level array layers.

* **Usage:**
```lopo
flatten([1, [2, [3]]]); # Returns [1, 2, 3]

```



### `unique(arr)` / `uniqueBy(arr, fn)`

Filters out and extracts duplicates elements out of target arrays.

### `count(arr, value)`

Counts precisely how many entries precisely match the specified evaluation structure parameter.

* **Usage:**
```lopo
count([1, 2, 2, 3], 2); # Returns 2

```



### `randomChoice(arr)`

Grabs an item completely at random out of an input vector collection.

---

## 5. Object Operations

### `has(obj, key)` / `hasOwn(obj, prop)`

Validates if an object explicitly maps specific property identities internally.

* **Usage:**
```lopo
has({name: "Lopo"}, "name"); # Returns true

```



### `keys(obj)` / `values(obj)` / `entries(obj)`

Transforms property items instantly out into standard indexed collections.

* **Usage:**
```lopo
keys({x: 1, y: 2}); # Returns ["x", "y"]

```



### `merge(obj1, obj2)` / `mergeDeep(obj1, obj2)`

Combines multiple objects into single structural outputs.

* **Usage:**
```lopo
merge({a: 1}, {b: 2}); # Returns {a: 1, b: 2}

```



### `invert(obj)`

Flips object configuration structures swapping properties with values fields.

* **Usage:**
```lopo
invert({key: "val"}); # Returns {val: "key"}

```



### `getProp(obj, path, fallback)` / `setProp(obj, path, value)`

Reads or assigns deeply nested value targets across string path markers.

* **Usage:**
```lopo
getProp(user, "profile.meta.id", "default");

```



---

## 6. Input/Output & Filesystem

### `ask(prompt)`

Synchronously halts execution to wait for human terminal interface keyboard input entries.

* **Usage:**
```lopo
define name = ask("Enter username:");

```



### `readFile(path)` / `writeFile(path, content)` / `appendFile(path, content)`

Synchronous file storage management operations handling reading and updates.

* **Usage:**
```lopo
define configuration = readFile("./config.json");
writeFile("./log.txt", "system operational activity entry");

```



### `exists(path)`

Returns boolean verification tracking file path access locations.

### `mkdir(path)`

Recursively creates file storage folder locations safely where they do not already exist.

### `deleteFile(path)` / `rmdir(path)`

Deletes specified file artifacts or targeted directory systems cleanly.

---

## 7. Networking, Servers & API Management

### `createServer(options)`

Launches highly interactive HTTP web applications equipped with custom routing, cookie processing mechanisms, dynamic content compilation engines, and live WebSocket synchronization options.

* **Usage:**
```lopo
define server = createServer({ enableWebSockets: true });

server.get("/api/user/:id", func(req, res) {
    return { userId: req.params.id, status: "active" };
});

server.listen(8080, func(port) {
    show "Application online at port " + str(port);
});

```



### `httpFetch(url, options)` / `fetch(url, options)`

Dispatches advanced web endpoint requests asynchronously towards external microservice interfaces.

* **Usage:**
```lopo
define response = await fetch("https://api.lopo.org/v1/status");
define data = await response.json();

```



### `get(url)` / `post(url, data)`

Quick-access abstraction helper channels executing explicit JSON payloads securely.

### `fetchApi(url, method, payloadString)`

A direct network call alternative tracking low-level network communications cleanly.

### `getIp()`

Detects active structural non-internal local area IPv4 machine routing addresses.

### `pingHost(host, port, timeout)`

Validates raw pipeline availability of remote structural system setups.

---

## 8. Serialization & Cryptography

### `JSONStringify(arg)` / `JSONParse(arg)` / `parseJson(arg)`

Utility converters translating structural variables back and forth over standard raw transport text lines. `parseJson` handles whitespace elegantly.

* **Usage:**
```lopo
define serialStr = JSONStringify({ active: true });
define dataObj   = parseJson(serialStr);

```



### `readJSON(path)` / `writeJSON(path, obj)`

Combined helper routines translating serialization actions straight toward disk structures directly.

### `encodeURLComponent(arg)`

Formats characters for safe URL transport.

* **Usage:**
```lopo
encodeURLComponent("hello world & users"); # "hello%20world%20%26%20users"

```



### `sha256(text)` / `cryptoSign(text, algorithm)`

Hashes text arguments into cryptographic security tracking strings.

* **Usage:**
```lopo
define trackingToken = sha256("secure secret access parameters");

```



---

## 9. System, Time & Global Objects

### `now()` / `timestamp()`

Returns standard Epoch Unix millisecond timestamps tracking active execution points.

### `sleep(ms)` / `delay(ms)`

Halts application loop executions non-blockingly for targeted durations via promises.

* **Usage:**
```lopo
await sleep(2000); # pauses code tracking for exactly 2 seconds

```



### `formatDate(timestamp, locale, options)`

Converts numeric timestamps into standardized human-readable calendar date layouts.

* **Usage:**
```lopo
define displayDate = formatDate(now(), "en-US", {});

```



### `getEnv(key, fallback)` / `envGet(key, fallback)`

Pulls operating environment tracking properties directly from system properties fields.

### Global Proxies: `Date` / `Math` / `String`

Gives custom runtime engines direct underlying native connectivity straight into baseline JS standard operations modules.