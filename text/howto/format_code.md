```js
function findX(num1, num2){
        let map = new Map();

        for(nums1 of num1){
            for(nums2 of num2){
                let diff = nums1 - nums2;
                if(map.has(diff)){
                    map.set(diff, map.get(diff)+1);
                }else{
                    map.set(diff, 1);
                }
            }
        }

        let xCandidate = [];
        for (let [key, value] of map.entries()){
            if(value == num2.length){
                x = key;
            }
        }

        for(nums1 of num1){
            for(nums2 of num2){
                if(nums1 + x == nums2){
                    return x;
                }
            }
        }
        return -x;
            
     }

     console.log(findX([4, 20, 16, 12, 8], [14, 18, 10])); // Output: -2
     console.log(findX([5, 32, 4, 16, 8], [2, 29, 13])); // Output: -3
     console.log(findX([4, 20, 16, 12, 8], [14, 18, 10])); // Output: -2
    console.log(findX([10, 20, 30, 40, 50], [12, 22, 32])); // Output: 2
    console.log(findX([5, 15, 25, 35], [20, 30])); // Output: 5
```
