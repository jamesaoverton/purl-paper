# Response to Reviewers

We would like to thank the reviewers for their helpful comments.

In the response below we have indicated quotations from the reviewers by prefixing lines with `>` (following the Markdown convention for blockquotes). We have indicated changes to the text by lines starting with "S", the section number, and the change. It may be more convenient to review changes on our GitHub repository for this paper at https://github.com/jamesaoverton/purl-paper


## Reviewer 1

> It would be nice to round out this information on what happened to the previously hosted information on purl.org & internet archive. One would imagine that some of the unclaimed purls must have been lost? Were the redirection targets captured for example, even when no longer resolvable? Such information could be useful to may to 'live' targets currently used by the new obo purls.

We have clarified that the OCLC system continued to run as a failover. Since OBO controlled the `obo` namespace at OCLC, and all our projects were below that, there was no concern about unclaimed PURLs.

S2.4. We added a sentence to clarify: "The OCLC system continued to run as a failover."
 
> w3id.org section:
> w3id.org.org system typo

S1.3. Fixed "w3id.org.org" -> "w3id.org"

> Implementation:
> 3 types of redirect cases are stated. It would be nice to add a concrete example for each if possible..I appreciate there is more information in the 'Testing and deployment' & 'Custom configuration' sections. Could alternatively direct reader to those sections and provide there.

S2.2. We added Listing 2 providing a `regex` example from the GO configuration file.

> custom configuration
> - if possible, it would be interesting to know the total number of 'term browsers' that are used to cover obo ontologies

S2.2. We added a sentence to clarify: "We are in the process of adding the Ontology Lookup Service as an alternative <a href="Jupp-2015"></a>, and eight projects use their own term browser." with citation for OLS.

> testing and deployment
> - couple of spaces after commas in a few locations

Unfortunately we were not able to find any such problems in the HTML for this section.

> - to automated the -> to automate the

S2.3 Fixed "to automated the deployment" -> "to automate the deployment"

> - If all test pass -> If all tests pass

S2.3. Fixed "If all test pass" -> "If all tests pass"

> Results
> - Is any more information on the 4xx errors available?

S3. We added a phrase to clarify: ", and most of these are simply malformed PURLs,"

> Future work
> Load balancing and backup/redundancy have been considered. Any thought to moving to entirely cloud-based solutions?

Our system is entirely cloud-based in the sense that we do not run any of our own hardware. We have intentionally avoided commitment to more "cutting-edge" cloud services in favour of tried-and-tested systems such as Apache.

> Web-based YAML editor sounds perfect.

Thank you.


## Reviewer 2

> Technical Quality:

> The authors have not demonstrated reusability by other organizations, either of how an organization might replicate this approach (does this work from the obo files or from OWL ontology files? What is the input, generally, to the yaml files used?), nor does it show an example of it being reused by a second organization. I would prefer to see such an evaluation, and possibly the reuse of the tool by another organization facing similar problems.

Our PURL system is indispensable the reuse of resources in the OBO community: without globally unique and persistent identifiers, our terms and ontologies would not be Findable and reuse would be difficult or impossible. We have 55 contributors from a range of different organizations using this system. The reuse of the PURL system itself, which consists of some configuration files and scripts, is not something that we consider a requirement or an indicator of success.

S2. We added a sentence to clarify that there is no restriction to ontology files: "Although our community has a focus on ontology files, the target of the redirect can be any resource that a URI can address."

> Novelty:

> While this is a useful contribution in technique, its simplicity makes it difficult to understand its novelty. It seems to be an incremental improvement over w3id, but one that might have been straightforward to discover with similar user cases. It might be helpful to understand what kinds of users have been able to contribute to these configurations - are they generally programmers, data scientists, biologists, or some mixture of that? If it turns out that most semi- and non-technical users are comfortable with this approach, that would be a novel and useful insight even beyond this single application.

We appreciate this criticism of the novelty of our approach. It is important to reiterate that we have deliberately avoided novel and "sexy" technologies in favour of a combination of tried-and-tested tools that we expect to still be available in ten years, or can easily replace. That said, we are not aware of another similar system.

To address the reviewer's point about who uses the system, we compiled a list of our 53 contributors other than the authors, most of whom we know personally, and classified them as "technical" or "non-technical" depending on whether they have a background in computer science or bioinformatics, or work in a software development role. We estimate that 14 of the 53 (26%) are non-technical on this classification.

S3. We added a sentence about non-technical users: "We estimate that at least a quarter of our contributors would not be able to reliably edit an `.htaccess` file directly, and thus our YAML configuration layer expands the number of contributors by at least that much."


## Reviewer 3

> Data availability: Not all used and produced data are FAIR and openly available in established data repositories; authors need to fix this

We are confused by this classification, since the other two reviewers said that "All used and produced data (if any) are FAIR and openly available in established data repositories". We will be happy to address the reviewer's concerns.

> Reasons to reject: 

> Listing to the Ansible implementation script itself is missing.

All our code and configuration is available on our public GitHub repository. We somehow omitted a link to that repository in the original submission, and have added it to the revised version. We believe that the Ansible script itself is too long and too peripheral to the main content of the paper, and so we have chosen not to include it as a listing.

S2. We added a clear link to our GitHub repository: "The git repository is hosted on GitHub, which provides a number of convenient features. If Github were to shut down" -> "The git repository is hosted on GitHub at <a href="https://github.com/OBOFoundry/purl.obolibrary.org">https://github.com/OBOFoundry/purl.obolibrary.org</a> (which is the target of the PURL <a href="http://purl.obolibrary.org">http://purl.obolibrary.org</a>). GitHub provides a number of convenient features, but if GitHub were to shut down"
            
> Further comments: 

> Listing 1 shows examples for "exact" and "prefix" but the text below speaks of "exact", "partial" and "regex". It takes some while to understand that it is actually an error and either "prefix" or "partial" is the correct term. Adding a regexp example to Listing 1 would have made it clearer.

Yes, the use of "partial" was a mistake -- it should be "prefix". We added Listing 2 as an example of a `regex` entry.

S2.2. Fixed "partial" -> "prefix" 


## Additional Minor Changes

S3. Updated "nearly one thousand commits" -> "more than one thousand commits"

S3. Fixed "caused a YAML file violate" -> "caused a YAML file to violate"

S5. Updated "54 contributors" -> "55 contributors"

S5. Updated "nearly 1000 changes" -> "more than one thousand changes"



