Intelligence sources are typically associated with the Collection & Processing stage of the Threat Intelligence Lifecycle. This is further subdivided into "Evaluation" and "Sources" sections.

Some intelligence sources may be better than others. We can judge them based on the following factors:

1. Timeliness - Ensures an intelligence source is up-to-date
2. Relevancy - Ensures an intelligence source matches its intended use case
3. Accuracy - Ensures an intelligence source produces effective results
4. Confidence Level - Ensures an intelligence source produces qualified statements about reliability

MISP Project codifies the use of the admiralty scale for grading data and estimative language.

- A. Reliable | <u>No doubt</u> of authenticity, trustworthiness, or competency; has a history of complete reliability.
- B. Usually Reliable | <u>Minor doubt</u> about authenticity, trustworthiness, or competency; has a history of valid information most of the time.
- C. Fairly Reliable | <u>Doubt</u> of authenticity, trustworthiness, or competency but has provided valid information in the past.
- D. Not Usually Reliable | <u>Significant doubt</u> about authenticity, trustworthiness, or competency but has provided valid information in the past. 
- E. Unreliable | <u>Lacking</u> in authenticity, trustworthiness, and competency; history of invalid information.
- F. Cannot Be Judged | <u>No basis</u> exists for evaluating the reliability of the source.

1. Confirmed | <u>Confirmed</u> by other independent sources; <u>logical</u> in itself; <u>consistent</u> with other information on the subject.
2.  Probably True | <u>Not Confirmed</u>; <u>logical</u> in itself; <u>consistent</u> with other information on the subject.
3. Possibly True | <u>Not Confirmed</u>; <u>reasonably logical</u> in itself; <u>agrees with some</u> other information on the subject.
4. Doubtfully True | <u>Not Confirmed</u>; <u>possible</u> but not logical; <u>no other information</u> on the subject.
5. Improbable | <u>Not Confirmed</u>; <u>not logical</u> in itself; <u>contradicted</u> by other information on the subject.
6. Cannot Be Judged | <u>No basis</u> exists for evaluating the validity of the information.

The main 3 types of sources are:

- Proprietary - Threat intelligence is very widely provided as a commercial service offering, where access to updates and research is subject to a subscription fee.
- Closed-Source - Data derived from the provider's own research and analysis efforts, such as data from honeynets that they operate, plus information mined from its customers' systems, suitably anonymized.
- Open-Source - Data that's available without subscription, which may include threat feeds, reputation lists, and malware signature databases. (US-CERT, UK's NCSC, AT&T Security OTX/AlienVault, MISP, VirusTotal, Spamhaus, SANS ISC, VXUG)

Threat feeds are a form of explicit knowledge, but implicit knowledge from experienced practitioners is also useful.

- OSINT - A method of obtaining information about a person or organization through public records, websites, and social media.