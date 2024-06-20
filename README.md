# Report Assignment 1 (Still Draft)
### By Group 6 : Voshon Fredison, Andreas Johannessen, Ivaylo Matsaliev, and Ties Schasfoort
## Project : [Geopandas](https://github.com/geopandas/geopandas)
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
  * File Path: SEP-group-6/geopandas/tests/test_version.py
  * File Tested Path: SEP-group-6/geopandas/_version.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/pull/6/commits/30015df96bbebacf17c9ecdb8dbcf7bc96e4a044)
  * ![v1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/print_coverage_percentage.png)
    
  * This is the tool I used to gather my own coverage percentage.
    The following is the added information for this function:
    
    ![v2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/coverage_flags.png)
    
    These are all the values I have used for the flags. For every branch in the function I have added the the following:
    
    ![v3](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/render_flags_examples.png)
    
    Now every time a branch gets executed I can take that into account and calculate the coverage.
    
    ![v4](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/render_branch_hit.png)

* **render_pep440(pieces: Dict[str,Any])**
  * File path: SEP-group-6/geopandas/tests/test_version.py
  * File tested path: SEP-group-6/geopandas/_version.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/pull/6/commits/4ec485c35c55182c3a561a3c1bd5de67b74b9e59)
  * For the second function, I have done the same:
    
    ![v5](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/coverage_flags_extra.png)
  * In this function there are fewer branches so I did not have to add many flags. I also did the same as I’ve done for the     previous one and that is to add the flags in each branch:
    
    ![v6](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/coverage_flags_extra_examples.png)
  * After all of this I was able to get another 100% branch coverage:
    
    ![v7](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/render_pep440_branch_hit.png)
### Coverage Improvement
* **render(pieces: Dict[str, Any], style: str)**
  * File path: SEP-group-6/geopandas/tests/test_version.py
  * File tested path: SEP-group-6/geopandas/_version.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/pull/6/commits/30015df96bbebacf17c9ecdb8dbcf7bc96e4a044)
  * Old coverage for _version.py:
    ![v8](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/old_cov_version.png)
  * New coverage:
    ![v9](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/new_cov_ver_render.png)
    
  * The percentage has increased by 18%. This is because there are not many misses anymore. The “render” function I have covered had a lot of branches that weren’t tested, so I made my test check all of the possible branches in that function.

* **render_pep440(pieces: Dict[str, Any])**
  * File path: SEP-group-6/geopandas/tests/test_version.py
  * File tested path: SEP-group-6/geopandas/_version.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/pull/6/commits/4ec485c35c55182c3a561a3c1bd5de67b74b9e59)
  * Old coverage for _version.py:
   ![v10](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/old_cov_version.png)
  * New coverage:  
   ![v11](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/new_coverage_version_render_pep440.png)
    
  * For this one, the coverage has not increased by much, because I haven’t used as many lines. It has only increased by 4%. Only a few extra lines have been covered which doesn’t increase the coverage percentage by a big amount.
In total, the coverage has increased to 40%:
  ![v12](https://github.com/Ties020/SEP-group-6/blob/main/report_images/voshi/total_version_coverage.png)

## Andreas
  * **_check_engine(engine, func)**
    * File path: SEP-group-6/geopandas/io/file.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/471b901ac9ceb74e993386c57ab807c96424eb0b)
    * Screenshot of coverage results:
      
      ![a1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/andy/andy_f1_1.png)
  * **_expand_user(path)**
    * File path: SEP-group-6/geopandas/io/file.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/471b901ac9ceb74e993386c57ab807c96424eb0b)
    * Screenshot of coverage results:
      
      ![a2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/andy/andy_f2_1.png)
  ### Coverage Improvement

## Ivaylo
  * **_tooltip_popup(type,fields,gdf,kwds)**
    * Path: SEP-group-6/geopandas/explore.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/3205f456bea68984624a3644865e8d983cf4c0da)
    * 
      ![i1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/ivo_f1_1.png)
    * The coverage is 0% due to the fact that the function is not tested at all.
  * **_ensure_geometry(data, crs)**
    * Path: SEP-group-6/geopandas/geodataframe.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/6608ab1e1b9203a54a92b10aad70516a87629788)
    * 
      ![i2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/ivo_f2_1.png)
    
    * The coverage is 0% due to the fact that the function is not tested at all.

### Coverage Improvement
  * **_tooltip_popup(type,fields,gdf,kwds)**
    * Path: SEP-group-6/geopandas/explore.py
    * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/45f26d3c10d4424a0ea6ad2a46ad8e88847abe42)
    * Old Coverage:
    
      ![i3](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/ivo_f1_1.png)
    * New Coverage:
    
      ![i4](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/ivo_impr1_1.png)
    * Initially, there were no prior tests for _tooltip_popup. As can be seen from the screenshots, the coverage improved by 100%.   For this specific function, most branches depend on the value of “fields”, thus all assert statements test the different values that fields can take. Furthermore, the parameter “type” can either be “tooltip” or “popup”, hence some of the asserts take one or the other. “gdf” is a GeoDataFrame object and there is a branch that depends on this object having specific attributes ("__plottable_column", "__folium_color"), hence we create a GeoDataFrame object with one of the columns.

* **_ensure_geometry(data, crs)**
  * Path: SEP-group-6/geopandas/geodataframe.py
  * Commit Link: [Commit](https://github.com/Ties020/SEP-group-6/commit/3e9be40007dd8f5cff5e19fd957d2cd4c0683abe)
  * Old Coverage:

     ![i5](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/ivo_f2_1.png)

  * New Coverage:

    ![i6](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ivo/ivo_impr2_1.png)

    * As with the previous function, prior to instrumentation, _ensure_geometry was not tested at all, hence the initial 0% coverage and 100% overall coverage improvement. The “data” parameter can take different types: GeoSeries, Series, GeometryArray and a simple list of Point objects. To improve coverage various assertions were added that pass one of the previously mentioned types. Furthermore, the parameter “crs” takes an integer value or can be omitted entirely. Whether this parameter is used or not also matters for which branches are hit, thus, a test is added in the scenario where crs is None. The “data” object may or may not have an attribute “crs”, which lead to certain branches being hit or not.


## Ties
 * **get_throttle_time(provider)**
   * Path: Group-6-SEP/geopandas/tools/geocoding.py
   
    ![t1](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/ties_f1_1.png)
 
   * In green you can see the code that was added to the geocode.py file to implement my own coverage tool.

   ![t2](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/ties_f1_2.png)
 
   * The screenshot above shows that the branch coverage in function one was 100% post-improvement.
* **_truncated_string(geom)**
  * Path: Group-6-SEP/geopandas/testing.py
 
    ![t3](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/ties_f2_1.png)

    * In the picture above you can see what lines were added to the testing.py file to implement my own branch coverage tool. The lines in green were added.
   
    ![t4](https://github.com/Ties020/SEP-group-6/blob/main/report_images/ties/ties_f2_2.png)

    * The screenshot above shows that the branch coverage in function 2 was 100% post-improvement. We’re only looking at the id’s trunc_branch_1 and trunc_branch_2 for this function.
   
  ### Coverage Improvement
  


