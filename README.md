This is a modified version of cinemaslides designed to create KDMs for existing CPLs. You can also specify an optional timezone for validity dates to make KDM management easier.

_Additional dependencies_: the gem 'tzinfo'. Install by running `gem install tzinfo`

_Usage_:
`cinemaslides --kdm --dkdm <path_to_dkdm> --cpl <path_to_cpl> --target <path_to_target> --zone "America/Vancouver" --start "2015-09-29T13:30:00" --end "2015-10-31T23:59:59"

Where _dkdm_ is the path to a DKDM targeted to the cinemaslides certificate. This allows cinemaslides to decrypt the CPL and access the content keys.

Where _cpl_ is the path to the Composition Playlist you'd like to generate the KDM for. You must produce a KDM for this CPL targeted to your cinemaslides key.

Where _zone_ is an optional timezone parameter. Specified in the plaintext format; see [this list](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) for reference.  The subsequent 'start' and 'end' time you specify will be converted into UTC time and used in the resulting KDM.

See [Digital Cinema Tools Distribution](https://github.com/wolfgangw/digital_cinema_tools_distribution/wiki) for an easy-to-use [Setup](https://github.com/wolfgangw/digital_cinema_tools_distribution/wiki/Setup) script. This will install everything required (batteries included).

See the [Wiki](https://github.com/wolfgangw/digital_cinema_tools/wiki) for notes and examples.

