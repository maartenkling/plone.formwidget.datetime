Changelog
=========

1.0b6 (2013-07-21)
------------------

- Fix javascript error in IE7/IE8 on Windows XP -> "Unable to modify the parent
  container element before the child element is closed"
  [href]

- Remove the ParameterizedWidgetFactory in favor of form schema hints for
  widget parameters which is available since plone.autoform 1.4.
  [thet]

- For the z3cform widget, remove widget adaptee registration from ZCML code and
  keep it in Python code. More appropriate z3c.form class hierarchy for the
  widget. Cleanup.
  [thet]

- Add autoinclude entry point.
  [thet]


1.0b5 (2013-05-27)
------------------

- Remove plone.app.jquerytools' custom.css again, as it is gone.
  [thet]

- Unify AT and DX templates.
  [thet]

- Fix issue when value has no timezone-information.
  This happened when using plone.app.event-dx and Solgema.fullcalendar
  [pbauer]


1.0b4 (2013-04-24)
------------------

- Don't show plone.formwidget.datetime:default profile when creating a Plone
  site with @@plone-addsite.
  [thet]

- Enable plone.app.jquerytools' custom.css for datepicker style overrides and
  enable next/prev icons this way.
  [thet]


1.0b3 (2013-02-08)
------------------

- Allow configuration of the first day of the week (first_day).
  [thet]


1.0b2 (2012-10-29)
------------------

- Fixed missing '00' in hour/minute in AT and z3cform for 0 values. Fixes #5.
  [thet]

- CSS fixes to display the calendar icon properly.
  [thet]


1.0b1 (2012-10-12)
------------------

- Include popup_calendar.gif and register a plone.formwidget.datetime style in
  the CSS registry.
  [thet]

- Changes related to "Archetypes widget now reliably returns DateTime instances
  instead datetime."

    - support for only year widget [kiorky]
    - Fix support for older years inside AT widgets [kiorky]
    - Add lot of tests for year ranges & old years [kiorky]
    - Fix the Year and Month/Years widgets [kiorky]

- Archetypes widget now reliably returns DateTime instances instead datetime.
  [thet]

- AM/PM 12-hour time fixes: 12 a.m. == u'00' hour internally, displayed
  consistently; normalization of times gracefully handles missing hour
  values; deal gracefully with 12 p.m. and 12 a.m. hours.
  [seanupton]

- Fixed a bug with the datepicker configuration when the week starts on
  a different day than Sunday.
  [dokai]

- Added a wrapper element around the time components in the z3c.form datetime
  widget markup to faciliate Javascript (and CSS) control.
  [dokai]

- Fixed a bug where the minutes were ignored and set unconditionally
  to zero when the field values were extracted.
  [dokai]

- Fixed a problem with zero valued time components being ignored.
  [dokai]

- Fixed a problem with the weekdays being off by one
  [href]

- fix all tests [kiorky]
- dynamic years range support [kiorky]
- support for very old years  ( <1800 ) [kiorky]
- support for custom date patterns in view mode [kiorky]


1.0a2 (2012-03-12)
------------------

- Include z3c.form's meta.zcml, so widgetsTemplate directive is registered.
  [thet]

- For conditional zcml incudes, use zcml:condition instead of zcml:provides.
  [thet]

- Code cleanup.
  [thet]


1.0a1 (2012-02-24)
------------------

- Initial alpha (!) release from the Plone Konferenz 2012 in Munich.
  [thet]


This package derived from collective.z3cform.datetimewidget. For older release
History, see there.
