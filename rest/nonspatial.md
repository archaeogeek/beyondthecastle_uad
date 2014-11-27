## Non-Spatial REST

Non-Spatial RESTful services are provided by [ArrestDB](https://github.com/alixaxel/ArrestDB) and can be accessed at [http://lancasteruad.oxfordarchaeology.com/rest/index.php](http://lancasteruad.oxfordarchaeology.com/rest/index.php). To access a particular table, use the form:

    http://lancasteruad.oxfordarchaeology.com/rest/index.php/tablename

See [https://github.com/alixaxel/ArrestDB](https://github.com/alixaxel/ArrestDB) for information on how to use this.

You can get information on, or query the following tables in the database:

###Spatial###

* **cellars**: dataset of Lancaster Buildings showing presence or absence of cellars - point
* **studyarea**: study area boundary of Lancaster Urban Archaeological Database project - multipolygon
* **listed_polys**: boundaries of listed buildings - multipolygon
* **event_points**: dataset representing historic or archaeological events - point
* **event_polys**: dataset representing the outline of events such as archaeological digs - multipolygon
* **mons_point**: dataset representing historic or archaeological monuments - point
* **monspres_polys**: dataset representing definite monument outlines, eg extant or exposed by archaeological events - multipolygon
* **monsint_polys**: proposed outlines of monuments based on information from archaeological research, events and other information - multipolygon
* * **geophys**: contour lines from geophysical survey - line (note this data has no attributes so might be best as base mapping)

###Non-Spatial###

**These are the principle tables in the database where the majority of information was stored**
* **tblBibliography** - bibliographic references used for events and monuments
* **tblDeposits** - deposits identified for use in deposit model
* **tblEvents** - archaeological events
* **tblEventsBibliography** - joins events (by Recevent_Number) and bibliographic records (by UAD_BIB_Number)
* **tblEventsMonuments** - joins events (by Recevent_Number) and Monuments (by Monument_Number)
* **tblExternalRefs_Events** - lists identifying codes or names for events in other databases
* **tblExternalRefs_Mon** - lists identifying codes or names for monuments in other databases
* **tblFieldworkers** - lists principle fieldworkers for archaeological events
* **tbl_mon_src** - joins monuments (by Internal_cross_ref_mon) to bibliographic sources (by Internal_cross_ref_src)
* **tblMonumentDates** - lists different phases of use for a monument
* **tblMonumentPeriods** - lists periods in which a monument was extant
* **tblMonuments** - monuments
* **tbl_monuments_listed** - lists monuments that are listed buildings
* **tblParentEvents** - lists events that comprise multiple smaller events such as large-scale archaeological investigations
* **tblParentEvents_events** - links parent events (by UAD_parent_EventID) to events (by UAD_Event_Number)
* **tblSubMonuments** - links collections of monuments together

###Lookups###

**These are descriptive tables, providing information on the terminology used in the tables above. Use them for reference only**
* tlkpArchiveTypes - lists different types of archaeological archive
* tlkpAreaStatus - lists different area designations with their abbreviation and full description 
* tlkpAssocOrganisations - lists the different archaeologicl/historical organisations that have done work in Lancaster
* tlkpAuthorsRole - lists different types of role with the creation of an archaeological archive or publication
* tlkpBookTypes - lists the different types of publication
* tlkpCurrDate - lists different ways of referring to the current date
* tlkpDatePrecision - lists different ways of referring to a date or date range in the past such as 'between', 'post', 'pre' etc
* tlkpDateTypes - lists different meanings for a date in the past, such as 'construction', 'disuse', 'use' etc
* tlkpDepositHorizons - lists different ways of describing a deposit horizon such as 'bottom', 'top', 'water' etc
* tlkpEventTypes - lists different types of archaeological event such as 'excavation', 'desk-based study' etc
* tlkpevidence - lists the different types of archaeological evidents such as 'wreckage', 'building', 'cropmark' etc
* tlkpExtInv - lists the different external inventories or databases that events and monuments may be listed in
* tlkpFieldworkerRole - lists the different roles a fieldworker may have in an archaeological investigation such as 'excavator', 'inspector', 'surveyor'
* tlkpItemNoQualifiers - lists different methods of referring to quantities of archaeological items and their precise meaning
* tlkpItemTypes - lists different types of archaeological item such as 'artefact', 'ecofact' etc
* tlkpMonDatePrecisions - lists different definitions of dates for time periods such as 'between', 'occasionally', 'throughout'
* tlkpNatGridPrecision - lists the different levels of precision of a National Grid Reference, such as 'within 1m', 'within 10m', 'within 1km' etc
* tlkpNGRQualifier - lists codes for determining what a Grid Reference actually refers to, such as the exact location of a find, the locality, the centre of a group of finds etc
* tlkpPeriods - lists the different time periods, their abbreviations, and their min and max dates where possible, such as 'Roman', 'Bronze Age', 'Post-Medieval' etc
* tlkpScientificDates - lists the different methods of obtaining a scientific date such as radiocarbon dating
* tlkpStatusQualifier - lists different methods of describing a location relative to another event or monument, such as 'adjacent to', 'excluded from' etc
* tlkp_Zconfidence - lists the level of confidence and the precision of any z (height) values

###Thesaurus###

**These are very specialist tables listing archaeological/historical terms and the relationships between them. Use them for reference only**
* THESAURUS_TERM_PREFERENCES - lists terms with their preferred terms
* THESAURUS_TERM_RELATION - lists related terms
* THESAURUS_TERMS - dictionary of archaeological/historic terms
* THESAURUS_TERM_USES - lists uses for terms
