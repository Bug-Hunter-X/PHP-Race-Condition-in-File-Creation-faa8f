# PHP Race Condition in File Creation

This repository demonstrates a common race condition in PHP that can occur when multiple processes or threads attempt to create a file simultaneously.  The provided code lacks proper locking mechanisms, leading to potential data loss or inconsistencies.  The solution showcases a robust approach using file locking to prevent such issues.

## Bug Description
The `bug.php` file shows a simple check-and-create approach for a file. If multiple requests hit this code at the same time, there is a race condition.  Both requests could pass the `file_exists` check, creating the file independently resulting in unexpected behavior and possible data loss.

## Solution
The `bugSolution.php` file addresses this by incorporating file locking, ensuring exclusive access during file creation. This prevents the race condition and guarantees the integrity of the file creation process.