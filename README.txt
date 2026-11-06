SS13 40.84.9 rebuilt source (July 2004, BYOND 338). Compiles with 0 errors to a .dmb that is CLOSE to the original
cellautomata.dmb (md5 b228461ed0231a0c12e97af466061d06, 680829 bytes) but NOT yet byte-identical:
audit DISTANCE 92 (types, map, objects, world, resources identical; every proc line matches; 5 procs differ in call
binding and 24 strings / 12 vars are in a different pool order - all compile timing, see C:\ss40849\NOTES.md).

Compiler: BYOND 338 (C:\s40\byond338\x), header "world bin v338 / min compatibility v338" as in the original.
  sh C:/ss40849/work/cmp.sh <folder>        (compiles <folder>/cellautomata.dme, prints md5 + audit against the original)
From scratch: sh C:/ss40849/work/rebuild2.sh <new folder>  (40.833 source from C:\misc\dev\space40833 + work\port40849.patch
  + map written from the 40.84.9 .dmb + icons from the 40.84.9 .rsc).

How it was made: the bit-perfect 40.833 source with every 40.833 -> 40.84.9 change put in: ~280 changed procs (3-way merge),
~180 new procs (capture-the-flag helper, ghost mob, fingerprint scanner/cards, proximity sensor + 3 assemblies, autolathe,
security records computer, portal/hand teleporter, paint, SWAT gear, ...), 31 new types, new vars (fingerprints, move_speed,
ctf, ...), the new changelog text, updated air-system values, 9 changed/new icons. Test.dm is gone in this version.
Where 40.93.0 (C:\misc\dev\space40930) has the same code its spelling was used.

Not the author's text: comments are gone (the .dmb does not store them); blank lines stand in for lines whose content
is unknown; some one-line settings / braced lines are choices that give the same bytes (see NOTES.md).
