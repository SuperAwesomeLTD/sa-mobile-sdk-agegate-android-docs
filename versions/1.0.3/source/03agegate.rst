Trigger the Age Gate
====================

In order to easily separate and direct users to different parts of your app based on their age, the Age Gate SDK has two simple methods:
One will add a callback that will notify you of the age the user has selected and one will actually trigger the Age Gate UI.

To set a callback:

.. code-block:: java

    import tv.superawesome.sdk.agegate.SAAgeGate;

    public class IntroActivity extends AppCompatActivity {

      @Override
      protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_intro);

        //
        // Set callback for the age gate
        SAAgeGate.setListener(new SAAgeGate.Interface() {
          @Override
          public void didEndAgeGate(int age) {
            // separate users
          }
        });
      }
    }

To trigger the age gate:

.. code-block:: java

  import tv.superawesome.sdk.agegate.SAAgeGate;

  public class IntroActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
      super.onCreate(savedInstanceState);
      setContentView(R.layout.activity_intro);

      //
      // ....

      //
      // start the Age Gate UI
      SAAgeGate.play(this);
    }
  }

Additionally you can override the display name and logo that's shown on the Age Gate:

.. code-block:: java

  public class IntroActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
      super.onCreate(savedInstanceState);
      setContentView(R.layout.activity_intro);

      //
      // override age gate display name
      SAAgeGate.overrideName("__MY_APP_NAME__");

      //
      // override age gate logo
      SAAgeGate.overrideLogo(R.drawable.__MY_APP_ICON__);
    }
  }

Finally, you should see something similar to the following images:

.. image:: img/AgeGate_1.png
.. image:: img/AgeGate_2.png

.. warning:: It's recommended to trigger the Age Gate as soon as your app starts, for example, in the first Activity.

.. note:: You can also find out the current stored user's age by asking **SAAgeGate.getCurrentAge();**
