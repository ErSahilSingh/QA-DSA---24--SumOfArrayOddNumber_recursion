# QA-DSA---24--SumOfArrayOddNumber_recursion

let arr = [5, 3, 2, 10, 1];
function sumFirstArr(nums) {
    let isodd = arr[nums] % 2 != 0
    if (nums === 0) {
        if (isodd) {
            return arr[0]
        } else {
            return 0
        }
    }
    if (isodd) {
        return arr[nums] + sumFirstArr(nums - 1)
    } else {
        return 0 + sumFirstArr(nums - 1)
    }
}

console.log(sumFirstArr(arr.length - 1))
