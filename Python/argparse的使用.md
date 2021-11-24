先mark一下argparse的简单用法，代码如下：
```python
# import argparse

parser = argparse.ArgumentParser(description='Test')
parser.add_argument('--batch_size', type=int, default=32, help='')
args = parser.parse_args()

print(args.batch_size)
```

