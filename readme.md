Øvelser i dag:
Vi skal sørge for at du kan finde ud af at kopiere koden og indsætte det og køre det så du kan teste at det virker før vi sender det
Så skal du også lære hvordan man gemmer filerne rigtigt
Bagefter så skal du øve det vi gennemgik sidste gang
Så runder vi af efter det



https://docs.google.com/document/d/16i61MkMsA9rZLdQsjwOlGG2fschtjcAWjLKgpl_heOw/edit?tab=t.0


import matplotlib.pyplot as plt
import matplotlib.animation as animation
import numpy as np
from IPython.display import HTML

fig, ax = plt.subplots(figsize=(6, 4))
ax.set_xlim(0, 10)
ax.set_ylim(0, 5)
ax.set_aspect('equal')

bold, = ax.plot([], [], 'o', markersize=20, color='red')

def opdater(frame):
    x = frame * 0.1
    y = abs(np.sin(frame * 0.2)) * 4
    bold.set_data([x % 10], [y])
    return bold,

ani = animation.FuncAnimation(fig, opdater, frames=200, interval=50, blit=True)
plt.close()
HTML(ani.to_jshtml())
