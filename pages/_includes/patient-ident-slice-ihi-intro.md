**Patient with Mandatory IHI** *[[Draft](http://hl7.org/fhir/r4/valueset-publication-status.html)]*

Prototype derived profile uses open slice (discriminator=type) to mandate one and only one IHI.

#### TBD
This profile is intended to use the discriminator of type – to do that we need to constraining the inherited discriminator. Have not yet been able to make this work.

As it stands to function equivalently to deriving from the Guidance only / Allowed Types there would need to be invariants to tighten up conformance. 

#### Test Examples

<table class="list" style="width:100%">
    <colgroup>
       <col span="1" style="width: 24%;"/>
       <col span="1" style="width: 25%;"/>
       <col span="1" style="width: 10%;"/>
       <col span="1" style="width: 10%;"/>
       <col span="1" style="width: 15%;"/>
    </colgroup>
	<tbody>
      <tr>
        <th>Test scenario</th>
        <th>resource id</th>
        <th>Expected</th>
        <th>Actual</th>
		<th>Notes</th>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-identifier-value-only-o.html">Patient with only identifier.value</a></td>
        <td>test-example-patient-identifier-value-only-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-identifier-o.html">Patient with identifier.value and system (uuid)</a></td>
        <td>test-example-patient-identifier-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-ihi-o.html">Patient with IHI</a></td>
        <td>test-example-patient-ihi-o</td>
        <td>Pass</td>
        <td>Pass</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-ihi-medicare-o.html">Patient with a valid IHI and a non-valid IHI and Medicare Number</a></td>
        <td>test-example-patient-ihi-medicare-o</td>
        <td>Fail</td>
        <td>Pass</td>
        <td>NOTE that when inheriting with profile, an 'invalid' IHI just reads as 'some other identifier type' so this won't fail an invalid IHI.</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-ihi-medicare-dva-o.html">Patient with IHI and Medicare Number and DVA number</a></td>
        <td>test-example-patient-ihi-medicare-dva-o</td>
        <td>Pass</td>
        <td>Pass</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-ihi-medicare-dva-mr-o.html">Patient with IHI and Medicare Number and DVA number and MRN</a></td>
        <td>test-example-patient-ihi-medicare-dva-mr-o</td>
        <td>Pass</td>
        <td>Pass</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-local-identifiers-o.html">Patient with HPI-O scoped MRN and Local namespace MRN</a></td>
        <td>test-example-patient-local-identifiers-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-medicare-testident-o.html">Patient with Medicare Number and a valid Patient Test Identifier</a></td>
        <td>test-example-patient-medicare-testident-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-testident-o.html">Patient with valid Patient Test Identifier</a></td>
        <td>test-example-patient-testident-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-medicare-o.html">Patient with Medicare Number</a></td>
        <td>test-example-patient-medicare-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-mult-medicare-testident-o.html">Patient with two Medicare Number and two valid Patient Test Identifiers</a></td>
        <td>test-example-patient-mult-medicare-testident-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-medicare-invalid-testident-o.html">Patient with a valid Medicare Number and a non-valid Patient Test Identifier with Identifier.system only</a></td>
        <td>test-example-patient-medicare-invalid-testident-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
      <tr>
        <td><a href="Patient-test-example-patient-medicare-testident-dva-o.html">Patient with Medicare Number, Patient Test Identifier and DVA number</a></td>
        <td>test-example-patient-medicare-testident-dva-o</td>
        <td>Fail</td>
        <td>Fail</td>
        <td>-</td>
      </tr>
    </tbody>
</table>
