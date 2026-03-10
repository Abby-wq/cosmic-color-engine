import random
import time
cosmic_colors = {
    "Nebula Pink": "#FF6EC7",
    "Supernova Gold": "#FFD700",
    "Galaxy Purple": "#6A0DAD",
    "Aurora Cyan": "#00FFFF",
    "Cosmic Indigo": "#4B0082",
    "Meteor Orange": "#FF4500",
    "Starlight Silver": "#C0C0C0",
    "Deep Space Blue": "#0B3D91",
    "Alien Green": "#39FF14",
    "Black Hole": "#0A0A0A"
}
def hex_to_rgb(hex_color):
    hex_color = hex_color.lstrip("#")
    return tuple(int(hex_color[i:i+2], 16) for i in (0, 2, 4))
def cosmic_loading():
    print("\n🌠 Scanning the universe for colors...\n")
    for i in range(5):
        print("✨", end="", flush=True)
        time.sleep(0.5)
    print("\n")
def generate_cosmic_color():

    name, hex_code = random.choice(list(cosmic_colors.items()))
    rgb = hex_to_rgb(hex_code)
    return name, hex_code, rgb
def main():
    print("""
╔════════════════════════════════════╗
        🌌 FLAVORTOWN COSMIC 🌌
     Random Galactic Color Engine
╚════════════════════════════════════╝
""")

    cosmic_loading()

    name, hex_code, rgb = generate_cosmic_color()

    print("🪐 Cosmic Color Discovered!")
    print("--------------------------------")
    print(f"🌟 Name : {name}")
    print(f"🎨 HEX  : {hex_code}")
    print(f"🔭 RGB  : {rgb}")
    print("--------------------------------")
    print("💫 Generated from the cosmic palette.\n")
if __name__ == "__main__":
    main()
