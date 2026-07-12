#network jammer 
import threading 
import datetime
import subprocess
wlan0 = subprocess.run(["ifconfig", "wlan0"], capture_output=True, text=True).stdout.strip()

class Kate:
    def __init__(self):
        self.lock = threading.Lock()
        self.last_run_time = None

    def launch(self):
        with self.lock:
            if self.last_run_time is None:
                print("Greeting br're lapin to Katerupter!")
            else:
                print("welcome back br're lapin to Katerupter!")
    def networks(self, command):
        subprocess.run(["ifconfig"])
        if command in ("search wlan station", "search wlan list", "near networks"):
            subprocess.run(["iwlist", "wlan0", "scan"])
            return "Searching for nearby networks..."
        scan = subprocess.run(["iwlist", "wlan0", "scan"], capture_output=True, text=True)
        if scan.returncode == 0:
            return "Nearby networks found " + scan.stdout + "!"
        return "Kate had a problem trying to find networks."

    def rupture(self, command):
        subprocess.run(["ifconfig"])
        if command in ("rupture" + wlan0, "jam" + wlan0):
            subprocess.run(["ifconfig", "wlan0", "down"])
            return "Jamming signal from " + wlan0 + "..."
        down = subprocess.run(["ifconfig", "wlan0", "down"], capture_output=True, text=True)
        if down.returncode == 0:
            return "signal jammed from nearby networks!"
        return "Kate had a problem trying to jam " + wlan0 + ":("

    def unrupture(self, command):
        if command in ("unrupture" + wlan0, "unjam" + wlan0):
            subprocess.run(["ifconfig", "wlan0", "up"])
            return "unjamming " + wlan0 + "..."
        up = subprocess.run(["ifconfig", "wlan0", "up"], capture_output=True, text=True)
        if up.returncode == 0:
            return wlan0 + " is back online! :)"
        return "Kate had a problem trying to unjam " + wlan0 + ":("
