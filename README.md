import os

# Emoji
robot = "🤖"
info = "ℹ️"
fail = "❌"

def check_device():
    print(f"{robot} Controllo dispositivi collegati...\n")
    output = os.popen("adb devices").read()
    dispositivi = [linea per linea in output.strip ().split (\n') [1:]se "dispositivo" in linea]
    
    se non dispositivi:
        print (f"{fail} Nessun dispositivo trovato. Verifica che ADB sia attivo e il telefono autorizzato.")
        Ritorno falso
    altrimenti:
        print (f"{info} Dispositivo rilevato:\n{devices[0]}\n")
        Ritorno vero

def get_device_info ():
    print (f"{info} Raccogliendo informazioni dal dispositivo...\n")

    Comandi = {
        "Modello": "Adb shell getprop ro.product.model",
        "Brand": "adb shell getprop ro.product.brand",
        "Versione Android": "Adb shell getprop ro.build.version.release",
        "Codice Build": "adb shell getprop ro.build.display.id",
        "IMEI (slot1) ": "servizio di shell adb call iphonesubinfo 1",
        "Seriale": "adb get-serialno",
        "CPU ABI": "adb shell getprop ro.product.cpu.abi",
        "Rete attiva": "Adb shell dumpsys netstats | grep iface",
    }

    per k, cmd in commands.items ():
        stampa (f"{robot} {k}:")
        sistema os.system (cmd)
        stampa ("")

 se ___ == "Nome____main__":
    vedi check_device ():
        get_device_info) 
