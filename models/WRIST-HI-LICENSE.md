# Wrist source geometry

BodyParts3D, Copyright 2008 Database Center for Life Science (DBCLS),
licensed under [CC Attribution-Share Alike 2.1 Japan](https://creativecommons.org/licenses/by-sa/2.1/jp/).
[Original DBCLS terms](https://lifesciencedb.jp/bp3d/info_en/license/index.html).

Sixteen original BodyParts3D / Anatomography 4.3 carpal OBJs from
[Oliver Case mirror](https://github.com/olivercase/body_parts_3d_api/tree/fd527e6f4daf732fd814314d9257df5877b844bc).
See `wrist-hi-source-lock.json` for exact filenames, FMA identities, sizes and SHA-256.
`wrist-hi.bin` and `wrist-hi.json` retain the same CC BY-SA 2.1 Japan licence.
Redistributions/adaptations must retain attribution, licence link, change notices
and applicable share-alike obligations. No author or institution endorsement.

Conversion: all vertices and triangles retained; common millimetre-to-metre
transform `[x/1000, z/1000 + 0.0781112, y/1000 - 0.00222675]`. Float32 positions,
normalized and reordered int16 normals, reversed triangle winding, uint32 indices.
No independent bone translation/scaling, generated mirror, smoothing, decimation
or segmented landmark. The viewer frames one explicitly selected side at a time,
with the same shared display transform as the existing atlas.

The `hi` name is a pack convention, not clinical resolution. Small coarse source
objects do not establish articular congruence, validated landmark boundaries,
soft tissue attachments or joint kinematics. Source-label/coordinate laterality
checks are not independent anatomical certification. Projection images derived
from this pack retain DBCLS attribution and CC BY-SA 2.1 Japan.

Reproduce: `node scripts/import-wrist-highres.mjs --fetch`, then offline read-only
`node scripts/import-wrist-highres.mjs --check`.
