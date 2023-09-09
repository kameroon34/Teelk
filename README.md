# Teelk $ npm install logo
API Key
GET YOUR API KEY
Endpoints
/search [POST]
Parameters
q	Query body
sort	popularity | newest | relevance
default: relevance
hide_low	When 1 passed, api skips results which has lower payout value than 0.05
default: 0
since	Allows to search result newer than a date.
Datetime in iso format (%Y-%m-%dT%H:%M:%S). e.g. 2019-09-19T13:11:00
default: null
scroll_id	While a search request returns a single "page" of results, the scroll_id can be used to retrieve large number of results. You can use current result set's scroll_id for pagination. Scroll ids are alive for 5 minutes.
Example Request
curl https://api.hivesearcher.com/search -d '{"q":"ecency", "sort": "newest"}' -H "Content-Type: application/json" -H "Authorization: YOUR_ACCESS_TOKEN" -X POST
Example Response
{
    "took": 0.031,
    "hits": 16687,
    "scroll_id": "DnF1ZXJ5VGhlbkZldGNoBQAAAAAAd77cFmY4TUc4Mlc2VGlxcnBZaFRNZkRlMlEAAAAAAA_TrhZUZVFlbGpfbFJ6aXpxUFdKRkF4dDBnAAAAAAAP068WVGVRZWxqX2xSeml6cVBXSkZBeHQwZwAAAAAAd77dFmY4TUc4Mlc2VGlxcnBZaFRNZkRlMlEAAAAAAHe-2xZmOE1HODJXNlRpcXJwWWhUTWZEZTJR",
    "results": [
        {
            "id": 64697517,
            "author": "ecency",
            "permlink": "ecency-the-best-and-fastest-app-on-hive-f19a641976f06est",
            "category": "ecency",
            "children": 29,
            "author_rep": 67.07,
            "title": "Ecency - The best and fastest app on Hive",
            "title_marked": "&lt;mark&gt;Marked&lt;/mark&gt; title of the post or comment",
            "body": "Full body text",
            "body_marked": "&lt;mark&gt;Marked&lt;/mark&gt; body of the post or comment",
            "img_url": "https://image.ibb.co/j1zzgL/header.png",
            "payout": 34.876,
            "total_votes": 419,
            "up_votes": 419,
            "created_at": "2018-10-22T06:47:15+00:00",
            "tags": [
                "ecency",
                "hive",
                "hive-dev",
                "hivesearcher",
                "search-engine"
            ],
            "app": "ecency/3.0.10-vision",
            "depth": 0
        },
        ...
    ]
}
