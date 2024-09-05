# NLT API Usage Documentation

From https://api.nlt.to/Documentation

The NLT API is based on HTTP GET requests with all parameters in the URL (unless noted as POST request). The output format is HTML (unless noted as, e.g., JSON).

Your API key is included in each request with the key query parameter. If _key=TEST_ or omitted, then your IP address will be used as a key, and you will be limited to 50 verses per request and 500 requests per day.

## https://api.nlt.to/passages

Return the Scripture text for the given passages, ordered by reference, as an HTML excerpt that can readily be included in a web page.

- **Example:** [https://api.nlt.to/api/passages?ref=John.1&key=TEST](https://api.nlt.to/api/passages?ref=John.1&key=TEST)
- **Query Parameters:**

    |   |   |
    |---|---|
    |ref|The reference(s) for the passages to be returned. More than one reference can be given, separated by semi-colons or commas.|
    |version|The Bible version to show. (Default _version=NLT_.) Available values:<br><br>\|   \|   \|<br>\|---\|---\|<br>\|NLT\|NLT (American English)\|<br>\|NLTUK\|NLT (UK English)\|<br>\|NTV\|Nueva Traducción Viviente\|<br>\|KJV\|King James Version\||
    |key|Your API license key.|


## https://api.nlt.to/api/search

Return search results (passages and short context paragraphs) for the given search query terms.

- **Example**: [https://api.nlt.to/api/search?text=mother+and+father&key=TEST](https://api.nlt.to/api/search?text=mother+and+father&key=TEST)
- **Query Parameters**:

    |   |   |
    |---|---|
    |text|The text to search for.|
    |version|The Bible version to search. (Default _version=NLT_.)|
    |key|Your API license key.|


## https://api.nlt.to/api/parse

Return a parsed list of references for the given reference string. _NOTE: the Content-Type for this query is always JSON._

- **Example**: [https://api.nlt.to/api/parse?ref=John.1&key=TEST](https://api.nlt.to/api/parse?ref=John.1&key=TEST)
- **Query Parameters**:

    |   |   |
    |---|---|
    |ref|The reference string to parse.|
    |key|Your API license key.|
    |language|The language. (Default _language=en_. Spanish is 'es')|


## https://api.nlt.to/api/plans

Return a list of reading plans supported by the API.

- **Example**: [https://api.nlt.to/api/plans?key=TEST](https://api.nlt.to/api/plans?key=TEST)
- **Query Parameters**:

    |   |   |
    |---|---|
    |key|Your API license key.|


## https://api.nlt.to/api/reading

Return the text for a given date in the given reading plan. (Default _date=today_.)

- **Example**: [https://api.nlt.to/api/reading?plan=OYB&key=TEST](https://api.nlt.to/api/reading?plan=OYB&key=TEST)
- **Query Parameters**:

    |   |   |
    |---|---|
    |plan|The name of the reading plan from which to retrieve the reading. The plan name should exactly match one of the reading plan names listed in [https://api.nlt.to/plans](https://api.nlt.to/api/plans)|
    |date|The date of the reading. (Default _date=today_.)|
    |version|The Bible version in which to provide the reading.|
    |key|Your API license key.|