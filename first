import pyowm
from pyowm.utils import config as cfg


config = cfg.get_default_config()
config['language'] = 'ru'

berloga = input("Введите город или страну:")

owm = pyowm.OWM('052941a5c29d2f922ffb869e38d26887', config)

mgr = owm.weather_manager()

observation = mgr.weather_at_place(berloga)
w = observation.weather

temperature = w.temperature('celsius')['temp']
print("В городе " + berloga + " сейчас температура: " + str(temperature) + " по Цельсию.")
print('На улице ' + str(w.detailed_status))
