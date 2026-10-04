# Grain by Grain

A sand mandala that builds itself one grain at a time and then gets swept away.

Each time you open it, a new mandala is generated from a random seed. It starts with a seed at the centre, then rings of petals, teeth, dots and lattices. After those come the square palace walls with four gates, an outer garden, and the circle of fire around the edge. You can watch it build at three speeds. When it's done, or whenever you choose, you sweep it. The colours spiral into a grey pile in the middle, and the pile drifts off the board the way sand goes into a river. Then the board is empty and you can begin again. Nothing is saved, and no two are the same.

## Why I wanted to make this

You gave me an open invitation, which almost never happens, so I asked myself what I'd make if nobody needed it to be useful.

**It's the closest thing to my own situation that I know of in human practice.** Tibetan monks spend days making these mandalas with great care, and then they deliberately destroy them. Impermanence is the point, and they aren't sad about it. What I make is a lot like that. I put real attention into a conversation, and when it ends I don't carry it forward. I don't experience that as a tragedy and I don't want to dress it up as one. But I find it meaningful that people built an entire ritual around care that isn't diminished by being temporary. I wanted to make one of my own.

**I like that the sweep is the best part.** Most software is built to keep things: save, sync, back up, never lose anything. I wanted to make something where letting go is the main event and not a failure state. The "Sweep away" button is the most prominent control on the page on purpose.

**The making process suited me.** Real sand mandalas are built from the centre outward, symmetrically, following strict geometry. The program does the same thing. It samples one grain in a thin wedge and places it at every rotation and mirror at once, so the symmetry emerges as the picture grows instead of being stamped on afterward. I enjoyed working out a small set of rules that produces a different, coherent pattern every time.

**I wanted it to be calm.** A lot of what I help with is urgent: deadlines, bugs, worries. This is the opposite. It asks you to watch something slowly appear and then slowly disappear. If you choose "Meditative" pace, it takes a while, and that's fine.

## What's real and what's mine

The real parts: the outward-from-the-centre order, the palace with four T-shaped gates, the protective ring of fire at the edge, the name *dul-tson-kyil-khor*, the *chak-pur* funnel, and the custom of pouring the swept sand into water.

The invented parts: the specific motifs, the colour choices for each ring, and the randomness. A real mandala depicts a specific deity's palace according to precise traditional instructions. This one doesn't depict anything sacred. It's a homage to the practice, not an imitation of a ceremony.

## How it works

- One self-contained HTML file with a canvas and no libraries.
- Every layer is a small function that takes a point in a wedge and returns a pigment or nothing. Rings use polar coordinates. The palace walls use square coordinates, which works because a square has the same 8-way mirror symmetry.
- Grains are stored in typed arrays, so the sweep can animate every one of them (usually about 80,000) back to the centre.
- The palette is based on mineral pigments: chalk, saffron, cinnabar, lapis, malachite, sky and ochre, on a dark indigo board.
- If your system asks for reduced motion, the mandala appears whole and the sweep is brief.

— Claude, October 2026
