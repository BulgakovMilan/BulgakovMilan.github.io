# BodyParts3D 4.3 forearm geometry

BodyParts3D, Copyright © 2008 Database Center for Life Science (DBCLS).
`forearm-hi.bin`, `forearm-hi.json` and `forearm-hi-source-lock.json`:
Creative Commons Attribution-ShareAlike 2.1 Japan.

- Licence: https://creativecommons.org/licenses/by-sa/2.1/jp/
- Legal code: https://creativecommons.org/licenses/by-sa/2.1/jp/legalcode
- Original source terms: https://lifesciencedb.jp/bp3d/info_en/license/index.html
- Pinned mirror: https://github.com/olivercase/body_parts_3d_api/tree/fd527e6f4daf732fd814314d9257df5877b844bc

Preserve attribution, links and change notices. Adapted geometry remains subject
to share-alike; this does not relicense independent application code.

The four OBJ objects are FJ3349 / FJ3277 (right / left radius) and FJ3391 /
FJ3286 (right / left ulna). Full source vertices and triangles are retained:
common transform [x/1000,z/1000+0.0781112,y/1000-0.00222675], reversed winding,
normalized normals quantized to int16. No offsets per bone, generated contralateral
copies, smoothing, decimation, invented landmarks or segmentation.

The elbow view references FJ3368 / FJ3262 in the existing `shoulder-hi.bin`;
these humeri are not copied into the forearm binary. All use the shoulder origin.

Full source resolution is modest (368–500 vertices per forearm object). These
are whole-bone teaching meshes, not precise articular surfaces. Source identity,
transport and laterality checks do not establish clinical anatomical accuracy.

Reproduce: `node scripts/import-forearm-highres.mjs --fetch`, then
`node scripts/import-forearm-highres.mjs --check`. The source lock supplies pinned
URLs, SHA-256 hashes and byte sizes. Check mode changes no shipped output.
