# README

数据集

1. Title: "Anonymous web data from www.microsoft.com"

2. Source Information
   -- Creators: Jack S. Breese, David Heckerman, Carl M. Kadie
     -- Microsoft Research, Redmond WA, 98052-6399, USA
     -- breese@microsoft.com, heckerma@microsoft.com, carlk@microsoft.com
   -- Donor: Breese, Heckerman, & Kadie
   -- Date: November 1998

3. Past Usage:
   -- J. Breese, D. Heckerman., C. Kadie _Empirical Analysis of
      Predictive Algorithms for Collaborative Filtering_ Proceedings
      of the Fourteenth Conference on Uncertainty in Artificial Intelligence,
      Madison, WI, July, 1998. 
	Also, expanded as Microsoft Research Technical Report MSR-TR-98-12,
	The papers are available on-line at:
             http://research.microsoft.com/users/breese/cfalgs.html
      -- Results: Used to compare various memory-based and model-based collobative
         filtering.
    - Predicted attribute: Goal was to predict what areas of the web site a
         user visited based on data on what other areas he or she visited.

4. Relevant Information:

    We created the data by sampling and processing the www.microsoft.com logs.
    The data records the use of www.microsoft.com by 38000 anonymous,
    randomly-selected users. For each user, the data lists all the areas of
    the web site (Vroots) that user visited in a one week timeframe.

    Users are identified only by a sequential number, for example, User #14988,
    User #14989, etc. The file contains no personally identifiable information.
    The 294 Vroots are identified by their title (e.g. "NetShow for PowerPoint")
    and URL (e.g. "/stream"). The data comes from one week in February, 1998.

    Dataset format:
	-- The data is in an ASCII-based sparse-data format called "DST".
           Each line of the data file starts with a letter which tells the line's type.
           The three line types of interest are:
               -- Attribute lines:
		     For example, 'A,1277,1,"NetShow for PowerPoint","/stream"'
                     Where:
                        'A' marks this as an attribute line,
                        '1277' is the attribute ID number for an area of the website
                                 (called a Vroot),
	                '1' may be ignored,
			'"NetShow for PowerPoint"' is the title of the Vroot,
                        '"/stream"' is the URL relative to "http://www.microsoft.com"
                -- Case and Vote Lines:
                    For each user, there is a case line followed by zero or more vote lines.
                     For example:
                           C,"10164",10164
                           V,1123,1
                           V,1009,1
                           V,1052,1
                      Where:
                         'C' marks this as a case line,
                          '10164' is the case ID number of a user,
                         'V' marks the vote lines for this case,
                         '1123', 1009', 1052' are the attributes ID's of Vroots that a
                                user visited.
                          '1' may be ignored.

5. Number of Instances:
      -- Training: 32711
      -- Testing:   5000
    Each instance represents an anonymous, randomly selected user of the web site.

6. Number of Attributes: 294

7. Attribute Information:
   Each attribute is an area ("vroot") of the www.microsoft.com web site.

   The datasets record which Vroots each user visited in a one-week timeframe
   in Feburary 1998.

8. Missing Attribute Values: The data is very sparse, so vroot visits are explicit,
    nonvisits are implicit (missing).

9. Class Distribution: 
    Mean number of vroot visits per case: 3.0