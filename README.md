# leetcode-217


1) bruce force:

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
                          else:
                                  return True
                  print(dict)
                  return False
                  
3) set - easiest:

           def containsDuplicate(nums):
                if len(nums) != len(set(nums)):
                        return True
                else:
                        return False

nums = [1,2,3,4]
I # nums = [1,2,3,1]
I # nums = [3,3]
print(containsDuplicate(nums))
