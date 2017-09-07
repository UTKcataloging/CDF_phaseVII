# OpenRefine Template for CDF Phase VII

---

## Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

## Row Template

```
{{'<mods xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">' 
+ '<identifier type="local">' + cells["identifier_adminDB"].value + '</identifier>' +
'<titleInfo><title>' + cells["title"].value + '</title></titleInfo>' +
if(isBlank(cells["identifier_isbn"].value),'', '<identifier type="isbn">' + cells['identifier_isbn'].value + '</identifier>') +
if(isBlank(cells["identifier_issn"].value),'', '<identifier type="issn">' + cells['identifier_issn'].value + '</identifier>') +
'<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2017113530">' + cells['repository'].value + '</physicalLocation></location>' +
if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>') +
'<relatedItem type="host" displayLabel="Digital Collection"><titleInfo><title>' + cells['project_title'].value + '</title></titleInfo></relatedItem>' +
'<originInfo><dateIssued>' + cells['dateIssued'].value + '</dateIssued>' +
if(isBlank(cells['publisher'].value), '', '<publisher valueURI="http://id.loc.gov/authorities/names/n80083301">' + cells['publisher'].value + '</publisher>') + '<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300026816">reports</form>' + if(isBlank(cells['extent'].value), '', '<extent unit="pages">' + cells['extent'].value + '</extent>') + '<digitalOrigin>reformatted digital</digitalOrigin></physicalDescription>
<language><languageTerm type="code" authority="iso639-2b">eng</languageTerm></language><typeofResource>text</typeofResource>'}} {{if(isBlank(cells['name_author 1'].value), '', '<name'+ if(isBlank(cells['name1_URI'].value), '', ' valueURI="' + cells['name1_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_author 1'].value + '</namePart>' + if(isBlank(cells['name_author 1'].value), '', '<role><roleTerm authority="marcrelator">Author</roleTerm></role>') + '</name>')}} {{if(isBlank(cells['name_author 2'].value), '', '<name'+ if(isBlank(cells['name2_URI'].value), '', ' valueURI="' + cells['name2_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_author 2'].value + '</namePart>' + if(isBlank(cells['name_author 2'].value), '', '<role><roleTerm authority="marcrelator">Author</roleTerm></role>') + '</name>')}}{{if(isBlank(cells['name_author 3'].value), '', '<name'+ if(isBlank(cells['name3_URI'].value), '', ' valueURI="' + cells['name3_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_author 3'].value + '</namePart>' + if(isBlank(cells['name_author 3'].value), '', '<role><roleTerm authority="marcrelator">Author</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_author 4'].value), '', '<name'+ if(isBlank(cells['name4_URI'].value), '', ' valueURI="' + cells['name4_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_author 4'].value + '</namePart>' + if(isBlank(cells['name_author 4'].value), '', '<role><roleTerm authority="marcrelator">Author</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['name_author 5'].value), '', '<name'+ if(isBlank(cells['name5_URI'].value), '', ' valueURI="' + cells['name5_URI'].value + '"' + ' authority="naf"') + '><namePart>' + cells['name_author 5'].value + '</namePart>' + if(isBlank(cells['name_author 5'].value), '', '<role><roleTerm authority="marcrelator">Author</roleTerm></role>') + '</name>')}}
{{if(isBlank(cells['subject_geographic'].value), '', '<subject><geographic' + if(isBlank(cells['URI_geo'].value), '>', ' valueURI="' + cells['URI_geo'].value + '">') + cells['subject_geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_topic_LCSH'].value), '', '<subject><topic' + if(isBlank(cells['URI_topic'].value), '>', ' valueURI="' + cells['URI_topic'].value + '">') + cells['subject_topic_LCSH'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_LCSH2'].value), '', '<subject><topic' + if(isBlank(cells['URI_topic2'].value), '>', ' valueURI="' + cells['URI_topic2'].value + '">') + cells['subject_topic_LCSH2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_topic_LCSH3'].value), '', '<subject><topic' + if(isBlank(cells['URI_topic3'].value), '>', ' valueURI="' + cells['URI_topic3'].value + '">') + cells['subject_topic_LCSH3'].value + '</topic></subject>')}} {{if(isBlank(cells['subject_topic_LCSH4'].value), '', '<subject><topic' + if(isBlank(cells['URI_topic4'].value), '>', ' valueURI="' + cells['URI_topic4'].value + '">') + cells['subject_topic_LCSH4'].value + '</topic></subject>')}} {{if(isBlank(cells['subject_topic_NAF'].value), '', '<subject><name' + if(isBlank(cells['URI_NAF_topic'].value), '>', ' valueURI="' + cells['URI_NAF_topic'].value + '">') + cells['subject_topic_NAF'].value + '</name></subject>')}} {{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}} {{'<recordInfo><recordContentSource>' + cells['record_source'].value + '</recordContentSource></recordInfo>'}} {{'<accessCondition type="use and reproduction" xlink:href="' + cells['rights_URI'].value + '>' + cells['rights'].value + '</accessCondition>'}}

```

## Row Separator

**LEAVE BLANK**

## Suffix

```
</modsCollection>

```