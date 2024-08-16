https://til.simonwillison.net/graphql/graphql-with-curl

https://simonwillison.net/2020/Oct/9/git-scraping/

https://github.com/marketplace/actions/gsheet-action

Historical data JSON -> CSV

cat scratch_153.json | jq -r '(.data.viewer.zones[0].httpRequests1dGroups.[] | [.dimensions.date,.avg.bytes,.sum.bytes,.sum.pageViews,.sum.requests,(.sum.ipClassMap[] | select(.ipType=="searchEngine").requests),.uniq.uniques]) | @csv' | pbcopy