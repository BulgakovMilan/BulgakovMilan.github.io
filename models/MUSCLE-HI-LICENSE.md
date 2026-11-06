# BodyParts3D 4.3 shoulder and arm muscles

BodyParts3D, Copyright © 2008 Database Center for Life Science (DBCLS).
Mesh data and these converted geometry packs: **Creative Commons Attribution-ShareAlike 2.1 Japan**.
Licence: https://creativecommons.org/licenses/by-sa/2.1/jp/
Legal code: https://creativecommons.org/licenses/by-sa/2.1/jp/legalcode
DBCLS source terms: https://lifesciencedb.jp/bp3d/info_en/license/index.html

Files: `muscle-deltoid-hi.bin`, `muscle-rotator-cuff-hi.bin`,
`muscle-biceps-brachii-hi.bin`, `muscle-triceps-brachii-hi.bin`, and accompanying
`muscle-hi.json` and `muscle-hi-source-lock.json` geometry metadata.
Retain attribution, source links, transformation notices and this licence when
redistributing or adapting the geometry. Adaptations remain under the applicable
share-alike terms. These notices do not relicense the independent application code.

Source mirror curated by Oliver Case:
https://github.com/olivercase/body_parts_3d_api/tree/fd527e6f4daf732fd814314d9257df5877b844bc
Individual asset URLs, original LFS SHA-256 hashes and sizes are in the source lock.
OBJ header identities and membership in the version-stamped FMA2Obj 4.3 manifest
are verified by `scripts/import-muscle-highres.mjs`. Some CSV group concept IDs
differ from the asset's own FMA ID; the importer uses the OBJ header and filename.

Changes: original vertices and triangles retained, common Y/Z axis swap, mm to m,
common translation, triangle winding reversal, unit normals stored as int16.
No per-object repositioning, invented surface segmentation or decimation.
Six bone position buffers match the existing 4.3 shoulder pack byte for byte.
No 4.0 skeletal geometry is mixed with these muscles. Neither the model nor
attachment locations have been reviewed by an anatomist.

The arm packs contain four biceps head objects and six triceps head objects,
plus bilateral scapulae and humeri as noninteractive context. Forearm bones,
tendon footprints, nerves and attachment-site segmentation are not included.
Source reproduction without overwriting outputs: `node scripts/import-muscle-highres.mjs --check`
(requires the pinned OBJ cache populated by `--fetch`).

The archive at dbarchive.biosciencedbc.jp has separate current CC BY 4.0 terms.
This pilot preserves the Anatomography site's BY-SA terms for its 4.3 exports;
it does not substitute the archive's licence for the downloaded files.
