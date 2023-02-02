def calculates(s,str)->int:
    stack=[]
    num=0
    sign=1
    result=0
    for c in s:
        if c.is digit():
            num=num*10+int(c)
        elif c in"+-":
            result+=sign*num
            num=0
            sign=1 if c=="+"else-1
        elif c=="*":
            stack.append(result)
            stack.append(sign)
            sign=1
            result=num
            num=0
        if num:
            result+=sign*num
    while stack:
        result*=stack.pop()
        result+=stack.pop()
    return result
