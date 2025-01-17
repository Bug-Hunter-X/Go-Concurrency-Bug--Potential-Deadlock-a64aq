# Go Concurrency Bug: Potential Deadlock

This repository demonstrates a potential deadlock scenario in Go, highlighting the importance of careful goroutine management when working with channels and wait groups. 

The `bug.go` file contains a Go program that illustrates a race condition.  The `bugSolution.go` file provides a corrected version, demonstrating how to avoid the issue.

## Bug Description

The `bug.go` program creates two goroutines. One goroutine sends values to a channel and the other goroutine receives values from that same channel.  Without proper synchronization, a deadlock could occur, if the second goroutine finishes its work before the first one manages to send all the values.

## Solution

The `bugSolution.go` file resolves this issue.