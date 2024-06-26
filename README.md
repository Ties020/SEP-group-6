# Report Assignment 1
### By Group 6 : Voshon Fredison, Andreas Johannessen, Ivaylo Matsaliev, and Ties Schasfoort
## Tools/Repos
### Selected Project : [Geopandas](https://github.com/geopandas/geopandas)
### Programming language: Python
### Counting Lines Tool : [Lizard](https://github.com/terryyin/lizard)
### Coverage Tool : [coverage.py](https://github.com/nedbat/coveragepy)
### Number of lines of code and the tool used to count it: 27257 NLOC
![nloc](https://github.com/Ties020/SEP-group-6/blob/main/report_images/nloc.png)



## Coverage Measurement
### Existing tool
We used coverage.py to compute the initial branch coverage of the entire project. Which led us to improving coverage on low-percentage functions:

![whole1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/whole_cover_before_1.png)
![whole2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/whole_cover_before_2.png)

## Voshon
* **render(pieces: Dict[str, Any], style: str)**
  * File: SEP-group-6/geopandas/_version.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/pull/6/commits/30015df96bbebacf17c9ecdb8dbcf7bc96e4a044)
    ![v1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/print_coverage_percentage.png)
    
  * This is the tool I used to gather my own coverage percentage.
    The following is the added information for this function:
    
    ![v2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/coverage_flags.png)
    
    These are all the values I have used for the flags. For every branch in the function I have added the the following:
    
    ![v3](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/render_flags_examples.png)
    
    Now every time a branch gets executed I can take that into account and calculate the coverage.
    
    ![v4](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/render_branch_hit.png)

* **render_pep440(pieces: Dict[str,Any])**
  * File: SEP-group-6/geopandas/_version.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/pull/6/commits/4ec485c35c55182c3a561a3c1bd5de67b74b9e59)
  * For the second function, I have done the same:
    
    ![v5](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/coverage_flags_extra.png)
  * In this function there are fewer branches so I did not have to add many flags. I also did the same as I’ve done for the previous one and that is to add the flags in each branch:
    
    ![v6](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/coverage_flags_extra_examples.png)
  * After all of this I was able to get another 85.7% branch coverage:
    
    ![v7](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/render_pep440_branch_hit_new.png)

  * It’s not 100% because I didn't test the hit the hidden “else” branches.
    
### Coverage Improvement
* **render(pieces: Dict[str, Any], style: str)**
  * Tested File: SEP-group-6/geopandas/_version.py
  * Test: SEP-group-6/geopandas/tests/test_version.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/pull/6/commits/30015df96bbebacf17c9ecdb8dbcf7bc96e4a044)
  * Old coverage:
    
    ![v8](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/old_cov_version.png)
  * New coverage:
    
    ![v9](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/new_cov_ver_render.png)
    
  * The percentage has increased by 18%. This is because there are not many misses anymore. The “render” function I have covered had a lot of branches that weren’t tested, so I made my test check all of the possible branches in that function.

* **render_pep440(pieces: Dict[str, Any])**
  * Tested File: SEP-group-6/geopandas/_version.py
  * Test: SEP-group-6/geopandas/tests/test_version.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/pull/6/commits/4ec485c35c55182c3a561a3c1bd5de67b74b9e59)
  * Old coverage:
    
    ![v10](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/old_cov_version.png)
  * New coverage:
    
    ![v11](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/new_coverage_version_render_pep440.png)
 
  * For this one, the coverage has not increased by much, because I haven’t used as many lines. It has only increased by 4%. Only a few extra lines have been covered which doesn’t increase the coverage percentage by a big amount.

In total, the coverage has increased to 40%:

  ![v12](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/total_version_coverage.png)

## Andreas
  * **_check_engine(engine, func)**
    * File: SEP-group-6/geopandas/io/file.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/471b901ac9ceb74e993386c57ab807c96424eb0b)
    * Screenshot of coverage results:
      
       ![a1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/andy/andy_f1_1.png)
      
  * **render_git_describe_long(pieces: Dict[str, Any])**
    * File: SEP-group-6/geopandas/_version.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/6d9cf9018d9069d539376f85c9370b43eef60541)
    * Screenshot of coverage results:
      
       ![a2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/andy/git_describe_long_coverage.png)
      
  ### Coverage Improvement
  * **_check_engine(engine, func)**
    * Tested File: SEP-group-6/geopandas/io/file.py
    * Test: SEP-group-6/test_cheng.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/471b901ac9ceb74e993386c57ab807c96424eb0b)
    * Old coverage:
      
       ![a3](https://github.com/Ties020/SEP-group-6/blob/main/report_images/andy/file_old_coverage.png)
    * New coverage:
      
       ![a4](https://github.com/Ties020/SEP-group-6/blob/main/report_images/andy/check_engine_new_percentage.png)
   
    * As can be seen from the screenshots above, the coverage increased from 68% to 91% after including the new test. The improvement is a consequence of an
       increase in the number of varying arguments supplied to the function as part of
       testing. Thus, more conditionals are evaluated to true and additional branches are reached.
       
 * **render_git_describe_long(pieces: Dict[str, Any])**
   * Tested File: SEP-group-6/geopandas/_version.py
   * Test: SEP-group-6/test_rgdl.py
   * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/6d9cf9018d9069d539376f85c9370b43eef60541)
   * Old coverage:

     ![a5](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/old_cov_version.png)
     
   * New coverage:

     ![a6](https://github.com/Ties020/SEP-group-6/blob/main/report_images/andy/render_git_new_percentage.png)

   * Comment
     * Unlike the first test, this test focused on a previously untested function, which naturally increases the overall coverage of the file when included.
      Specifically, the coverage increased from 40% to 41% (after Voshon increased the coverage from 18% to 40%).
     
## Ivaylo
  * **render_pep440_old(pieces: Dict[str, Any])**
    * File: SEP-group-6/geopandas/_version.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/9eaa676bbe30a08cf34722c818ff6d7c72f7e881)
      
      ![i1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/old_coverage.png)
      
    * The coverage is 0% due to the fact that the function is not tested at all.
     
  * **render_pep440_pre(pieces: Dict[str, Any])**
    * File: SEP-group-6/geopandas/_version.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/d121220c8eaa05d499693a8cbbdee6ad2a81f5d9)
      
      ![i2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/render_pep_old.png)
    
    * The coverage is 0% due to the fact that the function is not tested at all.

### Coverage Improvement
 * **render_pep440_old(pieces: Dict[str, Any])**
    * Tested File: SEP-group-6/geopandas/_version.py
    * Test: SEP-group-6/test_ivo.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/2fa779515d1bb1aec46f817ee9f299dc1556d4d4)
    * Old coverage:
      
      ![i3](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/version_old_coverage.png)
      
    * New coverage:
      
      ![i4](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/version_new_coverage_old.png)

* **render_pep440_pre(pieces: Dict[str, Any])**
  * Tested File: SEP-group-6/geopandas/_version.py
  * Test: SEP-group-6/test_ivo.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/861b64d22d760ad384221f928642e7d7c225a5ae)
  * Old Coverage:

     ![i5](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/version_old_coverage.png)

  * New Coverage:
   
    ![i6](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/version_new_cov_pre.png)

  * The coverage of _version.py has increased from 18% to 23%. 

The total coverage of _version.py has increased from 18% to 27% (before anyone else has improved the coverage of _version.py)

## Ties
 * **get_throttle_time(provider)**
   * File: SEP-group-6/geopandas/tools/geocoding.py
   
    ![t1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/ties_f1_1.png)
 
   * In green you can see the code that was added to the geocode.py file to implement my own coverage tool.

   ![t2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/ties_f1_2.png)
 
   * The screenshot above shows that the branch coverage in function one was 100% post-improvement.
* **_truncated_string(geom)**
  * File: SEP-group-6/geopandas/testing.py
 
    ![t3](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/ties_f2_1.png)

    * In the picture above you can see what lines were added to the testing.py file to implement my own branch coverage tool. The lines in green were added.
   
    ![t4](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/ties_f2_2.png)

    * The screenshot above shows that the branch coverage in function 2 was 100% post-improvement. We’re only looking at the id’s trunc_branch_1 and trunc_branch_2 for this function.
   
 ### Coverage Improvement
  * **get_throttle_time(provider)**
    * Tested File: SEP-group-6/geopandas/tools/geocoding.py
    * Test: SEP-group-6/geopandas/tests/test_geocoding.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/3f29b36d5337f43855255e4d241ba8308ff39c42)
    * Old Coverage:

       ![t5](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/geocoding_old.png)

    * New Coverage:
   
       ![t6](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/geocoding_new.png)

    * So, the total coverage of geocoding.py has increase by 4%.
      The branch coverage has increased from 50% to 100%. It has been improved by adding the test that also covers the if-statement below (with id throttle_branch_1):

       ![t7](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/get_throttle_imrpoved.png)
  
  * **_truncated_string(geom)**
    * Tested File: SEP-group-6/geopandas/testing.py:
    * Test: SEP-group-6/geopandas/tests/test_testing.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/1128962be504584ba59d999275bea2a2d6bfc59e)
    * Old Coverage:
   
       ![t8](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/testing_old.png)

    * New Coverage:
      
       ![t9](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/testing_new.png)

    * So, the total coverage of testing.py has increased by 2%.
      The branch coverage has increased from 50% to 100%. It has been improved by adding the test that also covers the if-statement below (with id trunc_branch_1):

       ![t10](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/truncated_string_improved.png)
      
## Overall
 ### Old overall coverage
   ![overall_old1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/whole_cover_before_1.png)
   ![overall_old2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/whole_cover_before_2.png)
   
 ### New overall coverage
   ![overall_new1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/new_overall_coverage1.png)
   ![overall_new2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/whole_cover_before_2.png)


## Individual Contributions
 ### Voshon
   * Reorganized inconsistencies in the report
 ### Andreas
   * Found the project
   * Made structural changes to the report
### Ivaylo
   * Converted the docx file to markdown
### Ties
   * Structure the report
   * Made the screenshots of coverage for all members to ensure consistency
