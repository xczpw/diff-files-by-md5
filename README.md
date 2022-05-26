# Diff Files By MD5
Check whether two files have the same content by md5


### Example:


```yaml
  Check:
    runs-on: ubuntu-latest
      - name: Source checkout
        uses: actions/checkout@v2

      - name: check
        id: check
        uses: xczpw/diff-files-by-md5@main
        with:
          file1: ./file1
          file2: ./file2
        
      - run: echo ${{ steps.check.outputs.result }}
```

If two files have the same md5, result will be **'same'**. Otherewise, result will be **'different'**.