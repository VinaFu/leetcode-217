# leetcode-217


1) bruce force/ out of time:

            def containsDuplicate(nums):
                  exist = []
                  for i in range(len(nums)):
                          if nums[i] not in exist:
                                  exist.append(nums[i])
                                  print(exist)
                          else:
                                  return True
                  return False

2) hash_table/ dict:

              def containsDuplicate(nums):
                  dict = {}
                  for val in nums:
                          if val not in dict:
                                  dict[val] = 1
                                  # why 1 ?
                          else:
                                  return True
                  print(dict)
                  return False
               
               ##my dict:
                    dict = {}
                    for i in range(len(nums)):
                            key = nums[i]
                            dict[key] = i
                            print(dict)
                            print(key)
                    for i in range(len(nums)):
                            if nums[i] in dict and dict[nums[i]] != i:
                                    return True
                    return False
                  
3) sorting:

             def containsDuplicate(self, nums: List[int]) -> bool:
                    l =  len(nums)
                    if l < 2:
                        return False
                    nums.sort()
                    for i in range(l-1):
                        if nums[i] == nums[i+1]:
                            return True
                    return False
                    

4) set - easiest:

           def containsDuplicate(nums):
                if len(nums) != len(set(nums)):
                        return True
                else:
                        return False

nums = [1,2,3,4]
I # nums = [1,2,3,1]
I # nums = [3,3]
print(containsDuplicate(nums))
