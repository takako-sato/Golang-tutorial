# Golang-tutorial


package main

import (
	"fmt"
	"math"
)

var i, j int = 1, 2
const Pi = 3.14

func split(sum int) (x , y int) {
	x = sum * 4 / 9
	y = sum - x
	return
}

func main() {
	fmt.Println(split(17))
	var c, python, java = true, false, "no!" 
	fmt.Println(i, j, c, python, java)
	// 関数内でないと暗黙的な宣言（:=）はできない。
	k := 3
	fmt.Println(k)

	// 初期値なしでは、ゼロ値が与えられる。(0/false/"")
	var in int
	var f float64
	var b bool
	var s string
	fmt.Printf("%v %v %v %q\n", in, f, b, s)

	// 型変換 int → float64
	var x, y int = 3, 4
	fl := math.Sqrt(float64(x*x + y*y))
	z := uint(fl)
	fmt.Println(x, y, z)

	// 型認識 (int/float64/complex128...)
	v := 42
	fmt.Printf("v is of type %T\n", v)

	// 定数(const)は := を使って宣言できない
	const World = "世界"
	fmt.Println("Hello", World)
	fmt.Println("Happy", Pi, "Day")
	const Truth = true
	fmt.Println("Go rules?", Truth)
}

/* -----------------------------------------------
基本型
ool
string
int
int8 int16 int32(= rune) int64
uint uint8(= byte) uint16 uint32 uint64 uintptr
float32 float64
complex64 complex128
--------------------------------------------------- */
