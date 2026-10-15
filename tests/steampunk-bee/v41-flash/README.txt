V41-FLASH — Steampunk Mechanical Bee
====================================

Open index.html in any modern browser (Chrome / Edge / Firefox / Safari).
Keep index.html as a single file — it is fully self-contained.

NETWORK
  The first load pulls Three.js r160.1, OrbitControls, lil-gui and the
  post-processing addons from cdn.jsdelivr.net via an import map.
  Everything else is generated in code:
    * all geometry      — procedural
    * all textures      — procedural (canvas + value-noise fBm)
    * environment map   — procedural equirectangular studio, PMREM-filtered
  There are no external models or image assets. If the CDN is unreachable
  the page shows an "Engine offline" panel instead of a blank screen.


CONTROLS (lil-gui, top right)
  Exploded View ........ 0.00 - 1.00   separates every part along the
                                       selected axis, with cyan leader lines
  Explode Axis ......... Radial | Axial | Hybrid
  Cyan Leaders ......... marching dashed leader lines + base markers
  Flap Frequency ....... 0 - 60 Hz     real frequency, delta-time driven
  Flight / Idle ........ also nudges the flap frequency to 42 Hz / 7 Hz
  Gear Speed ........... 0.1x - 5.0x
  Wireframe ............ all solid materials
  Lighting & Post ...... bloom, exposure, core glow, studio floor
  Motion & Detail ...... wing motion trails, auto-rotate
  Performance .......... render resolution, reset camera

  Keyboard:  H  hide/show the whole UI      R  reset the camera


NOTES ON THE MECHANISM
  Gears    Both clockwork trains are solved, not eyeballed. Each centre
           distance equals the sum of the two pitch radii, and each gear's
           initial rotation is derived from the meshing invariant

               psi_a + psi_b == 0.5 (mod 1),
               psi = (contactAngle - rotation) * teeth / 2*pi

           With omega_i = (-1)^i * (N_0 / N_i) * omega_driver this sum is
           time-invariant, so the teeth stay interlocked at every speed.

  Wings    Right-hand wings use true mirrored geometry (positions negated in
           Z, normals transformed by the same normal matrix, triangle winding
           reversed). Negating a mesh scale instead would render the brass
           vein tubes inside-out.

  Flap     Above ~25 Hz a display cannot show individual beats, so up to four
           phase-lagged ghost membranes fade in as the frequency rises. That
           is a visual trail only — the membrane itself always beats at the
           exact frequency shown in the GUI and in the HUD.


PERFORMANCE
  Roughly 150-250 draw calls and ~200k triangles, two shadow-casting lights,
  one transmissive pass (amber eyes + core dome) and a bloom chain.
  If the frame rate is low, drop "Resolution" to 0.75-1.0, turn "Wing Trails"
  to 0, or set "Bloom Strength" to 0 (which also bypasses the composer).
