## How to use Fragments

<a href="https://github.com/vishaltorgal/Fragments/raw/master/fragments.apk"><img src="https://github.com/vishaltorgal/SendingEmails/blob/master/dlapk.png" width="150" height="80" title="White flower" alt="Flower"></a>

<br>
<h6> Fragment 1 </h6>
<p style="text-align: center;"><img src="https://github.com/vishaltorgal/Fragments/blob/master/img1.png" alt="" width="300" height="450"/>&nbsp;</p>
  
<h6> Fragment 2 </h6>
<p style="text-align: center;"><img src="https://github.com/vishaltorgal/Fragments/blob/master/img2.png" alt="" width="300" height="450"/>&nbsp;</p>
<br><br>

```java

public class Fragment1 extends Fragment {

    Button bt_1;

    public View onCreateView(LayoutInflater inflater, ViewGroup container,
                             Bundle savedInstanceState) {
        View v = inflater.inflate(R.layout.fragment1, container, false);

        bt_1 = (Button) v.findViewById(R.id.bt_1);

        bt_1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                Fragment fragment = new Fragment2();
                if (fragment != null) {
                    FragmentManager fragmentManager = getFragmentManager();
                    fragmentManager.beginTransaction()
                            .replace(R.id.frame_container, fragment).commit();

                }
            }
        });

        return v;
    }
    
```
