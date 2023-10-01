Train Model:
pip install -r requirements.txt
gdown https://drive.google.com/uc?id=19LSrZHYQqJSdKgH8Mtlgg7-i-L3eRhbh
unzip ./D-Fire.zip
mkdir datasets/dfire_train datasets/dfire_train/trainA datasets/dfire_train/trainB datasets/dfire_test/ datasets/dfire_test/trainA datasets/dfire_test/trainB 
python train.py --dataroot ./datasets/dfire_train --name dfire --CUT_mode CUT

Generate output images:
python test.py --dataroot ./datasets/dfire_test --name dfire --CUT_mode CUT --phase train --num_test 1000
See ./results/dfire/ for the output images