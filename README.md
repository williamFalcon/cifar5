# CIFAR 5 demo

# Pull data

Download the dataset
```bash
git clone https://github.com/YoongiKim/CIFAR-10-images.git
```
Prune classes to have only 5
```bash
cd CIFAR-10-images

for phase in train test
do
    for class in automobile cat deer frog horse
    do
        echo "$phase/$class"
        rm -rf "$phase/$class"
    done
done
```

## Run demo

```bash
pip install -r requirements.txt
python project/lit_image_classifier.py --data_dir ../CIFAR-10-images
```
