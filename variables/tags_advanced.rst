.. MusicBrainz Picard Documentation Project

.. TODO: Expand definitions

.. TODO: Note which tags are not provided by Picard

:index:`Advanced Tags <tags; advanced>`
========================================

You can make additional tags available by enabling the :doc:`Use track relationships <../config/options_metadata>` and the
:doc:`Use genres from MusicBrainz <../config/options_genres>` settings in Picard.

.. note::

   Tags will not be created and will not be available as variables if there was no value retrieved for the tag
   from the MusicBrainz database.

.. note::

   Some of these tags are only supported for certain file types or tag formats.  Please see the :doc:`Picard Tag Mapping
   <../appendices/tag_mapping>` section for details.

.. _advanced_relationships:

Track Relationship Tags
--------------------------
If you enable tagging with "Use track relationships", you get these extra tags:

**arranger**

    Arranger Relationship Type (releases, recordings, works), Instrumentator Relationship Type, Orchestrator Relationship Type (*since Picard 0.10*)

**composer**

    Composer Relationship Type

**composersort**

    Composer Relationship Type's Sort Name

**conductor**

    Conductor Relationship Type (releases, recordings), Chorus Master Relationship Type (releases, recordings)

**djmixer**

    Mix-DJ Relationship Type (*since Picard 0.9*)

**engineer**

    Engineer Relationship Type

**license**

    License Relationship Type (releases, recordings) (*since Picard 1.0*)

**lyricist**

    Lyricist Relationship Type

**mixer**

    Engineer Relationship Type ("Mixed By") (*since Picard 0.9*)

**performer:<type>**

    Performer Relationship Type (releases - vocals/instruments, recordings - vocals/instruments), <type> can be "vocal", "guest guitar", "solo violin", …

    Orchestra Relationship Type (releases, recordings), <type> is "orchestra"

    Concertmaster Relationship Type (releases, recordings), <type> is "concertmaster"

**producer**

    Producer Relationship Type

**remixer**

    Remixer Relationship Type

**work**

    Work Name (*since Picard 1.3*)

**writer**

    Writer Relationship Type (*since Picard 1.0*). Not written to most file formats automatically.
    You can merge this with composers with a script like:

    .. code-block:: taggerscript

        $copymerge(composer, writer)

.. _genre_settings:

:index:`Genre Tags <tags; genre>`
----------------------------------

If you enable "Use genres from MusicBrainz", you get:

**genre**

    Genre information from MusicBrainz (*since Picard 2.1, earlier versions used folksonomy tags*)
