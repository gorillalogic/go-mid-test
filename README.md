# Go Mid-Level Developer Coding Test

This is the coding test for mid-level [Go](https://golang.org/) developers. Please fork this repository into your own account or download the code and push it into your own public repository.

# Fibonacci

Write the code for **Fibonacci** function in _fibonacci.go_ so the provided unit test works as expected.

## Unit test

Your code should pass the provided unit test successfully.

```go
package fib

import "testing"

func TestFibonacci(t *testing.T) {
	data := []struct {
		n    uint
		want uint64
	}{
		{0, 0}, {1, 1}, {2, 1}, {3, 2}, {4, 3}, {5, 5}, {6, 8}, {10, 55}, {42, 267914296}, {90, 2880067194370816120},
	}

	for _, d := range data {
		if got := Fibonacci(d.n); got != d.want {
			t.Errorf("Invalid Fibonacci value for N: %d, got: %d, want: %d", d.n, got, d.want)
		}
	}
}
```

**Plus**

> Create a documentation for the fibonacci.go using GoDoc tool. Should contain at least two call examples on the output documentation.
> Why the function can't be used to calculate Fibonacci(1200)?
> Create a command line program that calls the Fibonacci function outputs the first 20 fibonacci numbers and calculate the time it took to complete the task.

# PicSpy

Write a command line program that receives a URL as argument and lists all the images referenced in the HTML response. The program should support at least the following type of images: jpg, png and gif. It should write the image URLs one per line. Don't worry to support SVG, embedded images or images provided via CSS.

## Usage example

Input example:

```console
picspy https://somepage.com
```

Output example:

```console
Image 1: https://somepage.com/images/image001.jpg
Image 2: https://somepage.com/images/image002.jpg
Image 3: https://somepage.com/images/image003.jpg
```

**Plus**

> Upload your implementation to it's own git repository (could be any: Github, Gitlab or Bitbucket).
> Change the implementation to receive the argument using flags. It should support at least two flags: --page with the URL of the desired page and --version that should response with: picspy v1.0.0.
> Create your own html page with a gallery of images and host the implementation on any cloud provider service so you can use it to call the program.
