inimesed=["Dima", "Alex", "Oleg"]
rost=[190, 175, 186]

def lisamine(i,r):
    rost.append(input("Sisesta nimi: "))
    inimesed.append(int(input("Sisesta kasv: ")))
    return i,r

def keskmine(r):
    s=0
    for rost1 in r:
        s+=rost1
    k=round(s/len(r),2) 
    return k

def list1(i,r):
    for j in range(len(r)):
        print(i[j], "tema pikkus ", r[j])

def maximum(i,r):
    m=max(r)
    kes=i[r.index(m)]
    print(f"{kes} on koige pikkam, tema pikkus on {m}")

def delete(i,r):
    nimi = input ("Sisesta nimi, mis kustutsda vaja")
    if nimi in i:
        ind=i.index(nimi)
        print("dasasd")
        inimesed.remove(i[ind])
        return.remove(r[ind])
    else:
        print("nimi puudub")
    return i,r

def sort(i,r):
    n=int(input("1-A-Z voi 2-Z-A"))
    m=input("i-inimeset sorteerimine, r-rost sorteerimine")
    if (n==1 and m=="i"):
        k=len(i)
        a="";o=0
        for j in range(0, k-1):
            for h in range(j+1,k):
                if i [j]>i[h]:
                    a=i[j]
                    i[j]=i[h]
                    i[h]=a
                    o = r[j]
                    r[j] = r[h]
                    r[h] = 0

def menu(i,r):
    v=input("Menu: \nadd \nkeskmine \nmaximum \ndelete \nsort \nlist \n")

    if v=="add":
        i,r=lisamine(inimesed,rost)
    elif v=="keskmine":
        k=keskmine(rost)
        print("dasdas")
    elif v=="maximum":
        maximum(inimesed,rost)
    elif v=="delete":
        i,r=delete(inimesed,rost)
    elif v=="sort":
        sort(inimesed,rost)
    elif v=="list":
        list1 (inimesed,rost)
        



while True:
    menu(inimesed,rost)
