Here is the updated README with the acknowledgment included inside the document:

---

# Urless

Urless is a simple tool developed in Go to test potential vulnerabilities in URL paths. It progressively removes the paths from a URL, leaving only the domain and generating variations with different directory depths.

## Installation

```bash
git clone https://github.com/KingOfBugbounty/urless.git
cd urless
go build -o urless
```

## Usage

Urless receives URLs via `stdin` and prints variations with different path levels.

### Example Usage

```bash
echo "https://example.com/dir1/dir2/dir3" | ./urless
```

### Expected Output

```
https://example.com
https://example.com/dir1/dir2/dir3
https://example.com/dir1/dir2
https://example.com/dir1
```

## Example with multiple URLs

```bash
cat urls.txt | ./urless
```

Where `urls.txt` contains:
```
https://site.com/a/b/c
https://another.com/x/y/z
```

The output will be:
```
https://site.com
https://site.com/a/b/c
https://site.com/a/b
https://site.com/a
https://another.com
https://another.com/x/y/z
https://another.com/x/y
https://another.com/x
```

## License

This project is licensed under the MIT License.

## Acknowledgments

A special thanks to @erickfernandox for the insightful vision and contribution to the development of this tool!

---

Let me know if you need further changes!
