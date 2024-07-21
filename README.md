# An Introduction to me

Hello, I'm Liam.  As a data analyst, I mostly create dashboards that increase the business capabilities of internal customers by given them insights into the data they previously didn't have access to.  

Other things I have done: created API data connections to external sources; designed a data governance strategy for a data warehouse that requires standardized naming of columns across production database tables, documentation for all production database objects, and code ownership and change logging; and built a data warehouse following that data governance strategy.

## My process for data analysis / making data products
For data analytics, I follow iterative P.A.C.E. project lifecycle:
<oi>
  <li>
    Plan: gather project requirements.  Talk with internal customers of project deliverables about the motivations behind the project, the "Why" that drove the internal customer(s) to request a report to be  made.
  </li>
  <li>
    Analysis: conduct exploratory data analysis.  For data products, this means using my knowledge of the busienss to find the data needed for the outlined business capabilities in the project requirments. 
For a quick analysis to answer a business question, I look for as many insights as are relevant to the requested information.
  </li>
  <li>
    Construct: finalize the viualizations of the data product, or pair down insights to a valuable few.
</il>
  <li>
    Execute: present the insights / data product to internal customers, get feedback, and make any changes if necessary
  </li>
</oi>

## My thoughts on data warehouse architecture and data governance (not big data)
<oi>
  <li>
    No NULLs: requiring an absence of nulls means that there are no problems with comparison operators or math functions.  Null = NUll returns neither true or false.
  </li>
  <li>
    Make tables as narrow as possible: This is mainly a source data entity problem, but tables should only contain as many rows as are necessary.
  </li>
  <li>
    MD5 or greater hashed primary and foreign keys: These primary and foreign keys should almost always be surrogate keys, and MD5 is faster than text for joining on, and has the added benefit of obfuscating the surrogate key elements for end-users.  Before you say it, collision is a possibility for MD5, but the chance is so incredibly small it is not likely to occur in most siutations.  MD5 is 128-bit, meaning there is a 50% chance of collision after <a href = "https://en.wikipedia.org/wiki/Birthday_problem#:~:text=%C3%971019-,2.2%C3%971019,-3.1%C3%9710"> 2.2x10<sup>19</sup> </a> hash values, or <a href = "https://preshing.com/20110504/hash-collision-probabilities/#:~:text=64%2Dbit%20or-,160%2Dbit,-%2C%20the%20following%20table">1.42x10<sup>24</sup></a> for SHA1.
  </li>
</oi>
